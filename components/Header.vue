<template>
  <header>
    <ul>
      <li><nuxt-link to="/">Starting page</nuxt-link></li>
      <li><nuxt-link to="/recipes">Recipes</nuxt-link></li>
      <li><nuxt-link to="/about">About</nuxt-link></li>
    </ul>
  </header>
</template>

<style scoped>
header {
  width: 100%;
  height: 30px;
  display: flex;
  justify-content: center;
  align-items: center;
  background: #512a43;
}

ul {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  justify-content: center;
  align-items: center;
}

li {
  margin: 0 10px;
}

a {
  color: white;
  text-decoration: none;
}
</style>
