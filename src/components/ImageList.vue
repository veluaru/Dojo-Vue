<template>
  <v-container>
    <v-card class="ma-5" max-width="600" v-bind:key="item.id" v-for="item in items.hits">
      <v-row>
        <v-col>
          <img class="ma-2" :src="item.previewURL" alt />
        </v-col>
        <v-col>
          <v-card-title>Propiedad de {{item.user}}</v-card-title>
          <v-card-subtitle>Tags: {{item.tags}}</v-card-subtitle>
        </v-col>
      </v-row>
    </v-card>
  </v-container>
</template>

<script>
export default {
  name: "ImageList",
  props: ["items"],
};
</script>