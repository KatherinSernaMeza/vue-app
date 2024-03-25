<template style="height: 100%;">
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
 html, body, #__nuxt, #__layout, [data-v-inspector="app.vue"], #app, main {
      height: 100%;
      margin: 0;
      padding: 0;
      background: red;
    }
</style>
