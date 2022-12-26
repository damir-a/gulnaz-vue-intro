<template>
  <div>
    <p>Author: {{ comment.email }}</p>
    <div>{{ comment.body }}</div>
  </div>
</template>

<script setup>
const props = defineProps({
  comment: Object,
})
</script>

<style scoped>

p {
  display: block;
  padding: auto;
  margin-left: 2px;
  border: 1px solid gray;
}
</style>
