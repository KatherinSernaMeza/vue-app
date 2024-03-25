<template>
  <header>
    <nav>
      <v-toolbar :elevation="8" title="Movies">
        <v-btn><NuxtLink  to="/">HOME</NuxtLink></v-btn>
        <v-btn> <NuxtLink  to="/Movies">MOVIES</NuxtLink></v-btn>
        <v-btn><NuxtLink  to="/Login">LOGIN</NuxtLink></v-btn>
    </v-toolbar>
    </nav>
  </header>
</template>

<script>
export default {};
</script>

<style></style>
