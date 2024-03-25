<template>
  <v-container class="bg-surface-variant container">
    <v-card class="bg-purple-darken-2 v-card w-100">
    <v-row
      class="mb-6"
      no-gutters
    >
      <v-col
        lg="6"
        md="12"
        sm="12"
        xs="12"
        cols = "12"
      >
        <v-sheet class="pa-2 ma-2">
          .v-col-sm-5 .v-col-md-6
        </v-sheet>
      </v-col>
      <v-col
        lg="6"
        md="12"
        sm="12"
        xs="12"
        cols = "12"
      >
        <v-sheet class="pa-2 ma-2">
          .v-col-sm-5 .offset-sm-2 .v-col-md-6 .offset-md-0
        </v-sheet>
      </v-col>
    </v-row>
</v-card>
  </v-container>
</template>

<script>
definePageMeta({
  layout: "custom",
});
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
