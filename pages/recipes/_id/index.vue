<template>
  <section class="single-recipe">
    <h1>{{ recipe.title }}</h1>
    <div>
      <img class="image-recipe" :src="recipe.thumbnail" :alt="recipe.title">
    </div>
    <p>{{ recipe.descriptionText }}</p>
  </section>
</template>

<script>
export default {
  asyncData(context) {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          recipe: [
            {
              id: "1",
              title: "Lawar",
              previewText: "Nasi lawar so delicous",
              descriptionText: "Just another description text",
              thumbnail: "https://3.bp.blogspot.com/-KLTp7cjSYV4/WCAVMrDOsoI/AAAAAAAABdw/ddrT_Ni_hYkOUlNgh95SnklEIoEQbGOpwCLcB/s1600/wrjambe.jpg"
            },
            {
              id: "2",
              title: "Babi Guling",
              previewText: "Babi Guling nyummy",
              descriptionText: "Just another description text",
              thumbnail: "http://www.letspaw.com/wp-content/uploads/2017/12/Lawar-Kuwir.jpg"
            }
          ].find(el => el.id === context.params.id)
        })
      }, 1500)
    })
  }
}
</script>

<style scoped>
.image-recipe {
  width: 100%;
}
.single-recipe {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  flex-flow: column;
  padding: 30px;
}
</style>
