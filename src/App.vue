<script setup>
import Post from './components/Post.vue';
</script>

<template>
  <suspense>
    <template #default>
      <Post :post_id="1" />
    </template>
    <template #fallback>
      <div>
        Loading...
      </div>
    </template>
  </suspense>
</template>

<style scoped>

</style>
