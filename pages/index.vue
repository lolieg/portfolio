<template>
  <div>
    <h1>{{ post.title }}</h1>
    <p>{{ post.description }}</p>
    <NuxtLink to="/lmao"></NuxtLink>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  async asyncData({ app }) {
    const post = await app.$http.$get(`https://api.nuxtjs.dev/posts/${1}`)
    return { post }
  },
})
// ...
</script>

<style>
.red {
  color: red;
}
</style>
