<template class="h-screen">
  <div id="app">
    <Nav />
    <main>
      <slot />
    </main>
    <footer></footer>
  </div>
</template>

<script>
import Nav from "@/components/Nav.vue";
export default {};
</script>

<style>
/* Estilo para todos los elementos padres hasta el html y el body */
html,
body,
[data-v-inspector="app.vue:2:3"],
#app,
main {
  height: 100%;
  margin: 0;
  padding: 0;
}
#__nuxt {
  height: 100%;
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
</style>
