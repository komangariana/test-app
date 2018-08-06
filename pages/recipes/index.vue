<template>
  <section class="recipes">
    <Recipe
      v-for="recipe in recipes"
      :key="recipe.id"
      :thumbnail="recipe.thumbnail"
      :title="recipe.title"
      :id="recipe.id"
      :previewText="recipe.previewText"
    />
  </section>
</template>

<script>

import Recipe from '@/components/Recipe'

export default {
 components: {
   Recipe
 },
 asyncData() {
   return new Promise((resolve, reject) => {
     setTimeout(() => {
       resolve({
         recipes: [
           {
             id: "1",
             title: "Lawar",
             previewText: "Nasi lawar so delicous",
             thumbnail: "https://3.bp.blogspot.com/-KLTp7cjSYV4/WCAVMrDOsoI/AAAAAAAABdw/ddrT_Ni_hYkOUlNgh95SnklEIoEQbGOpwCLcB/s1600/wrjambe.jpg"
           },
           {
             id: "2",
             title: "Babi Guling",
             previewText: "Babi Guling nyummy",
             thumbnail: "http://www.letspaw.com/wp-content/uploads/2017/12/Lawar-Kuwir.jpg"
           }
         ]
       })
     }, 1500)
   })
 }
}

</script>

<style scoped>
a {
  text-decoration: none;
  color: #000;
}
.recipes {
  display: flex;
  flex-flow: row wrap;
  justify-content: center;
  align-items : center;
}


</style>
