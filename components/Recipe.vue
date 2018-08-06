<template>
  <nuxt-link :to="'/recipes/' + id ">
    <article class="recipe">
      <div class="thumbnail" :style="{backgroundImage: 'url('+thumbnail+')'}"></div>
      <h1>{{ title }}</h1>
      <p>{{ previewText }}</p>
    </article>
  </nuxt-link>
</template>

<script>
export default {
  props: ['thumbnail', 'title', 'previewText', 'id']
}
</script>


<style scoped>
.recipe {
  box-sizing: border-box;
  border: 2px solid #000;
  width: 230px;
  padding: 8px;
  margin: 8px;
}

.thumbnail {
  background-position: center;
  background-sixe: cover;
  width: 100%;
  height: 200px;
}
</style>
