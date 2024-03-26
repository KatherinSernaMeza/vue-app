<template>
  <v-container class="bg-surface-variant container">
    <v-card class="bg-purple-darken-2 v-card w-100">
      <v-row class="mb-6" no-gutters>
        <v-col lg="6" md="12" sm="12" xs="12" cols="12">
          <v-sheet class="pa-2 ma-2">
            <DetailData />
          </v-sheet>
        </v-col>
        <v-col lg="6" md="12" sm="12" xs="12" cols="12">
          <v-sheet
            class="pa-2 ma-2"
            v-for="data in datas"
            :key="data.id"
            @click="getIdValue(data.id)"
          >
            <NuxtLink :to="`data/${data.id}`"> {{ data.title }} </NuxtLink>
          </v-sheet>
        </v-col>
      </v-row>
    </v-card>
  </v-container>
</template>

<script setup>
import DetailData from "@/components/DetailData.vue";
definePageMeta({
  layout: "custom",
});
const datas = ref([]);
let id = ref(0);
const loading = ref(false);
const error = ref(null);

onMounted(async () => {
  loading.value = true;
  try {
    // Realiza la solicitud GET utilizando $fetch
    const response = await $fetch("https://jsonplaceholder.typicode.com/posts");
    datas.value = response.slice(0, 10); // Suponiendo que la respuesta tiene una propiedad 'items'
  } catch (e) {
    error.value = e;
  } finally {
    loading.value = false;
  }
});
const getIdValue = (idData) => {
  // Implementación de tu método
  id = idData;
};
</script>

<style>
.container {
  height: 90vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
.v-card {
  height: fit-content;
}
</style>
