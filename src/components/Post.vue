<script setup>
import Comment from './Comment.vue';

const props = defineProps({
  post_id: Number,
});

const data = await fetch(`https://jsonplaceholder.typicode.com/posts/${props.post_id}`);
const post = await data.json();
const comments = await fetch(`https://jsonplaceholder.typicode.com/posts/${props.post_id}/comments`);
const comment = await comments.json();

</script>

<template>
  Post number {{ post.id }}
<div>
  <p>{{ post.title }}</p>
  <div>{{ post.body }}</div>
</div>
<div>Comments:</div>
<div v-for="c in comment">
  <Comment :comment="c" />
</div>
</template>

<style scoped>

</style>
