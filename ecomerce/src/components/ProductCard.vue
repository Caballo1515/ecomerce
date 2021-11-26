<template>
  <v-card class="mx-auto" max-width="344" outlined>
    <v-list-item three-line>
      <v-list-item-content>
        <div class="text-overline mb-4">
          {{ product }}
        </div>
        <v-list-item-title class="text-h5 mb-1">
          {{ price }}
        </v-list-item-title>
        <v-list-item-subtitle>{{ description }}</v-list-item-subtitle>
      </v-list-item-content>
      <v-img
        lazy-src="https://picsum.photos/id/11/10/6"
        max-height="80"
        max-width="80"
        src="https://picsum.photos/id/11/500/300"
      ></v-img>
    </v-list-item>

    <v-card-actions>
      <v-btn outlined rounded text> Button </v-btn>
    </v-card-actions>
  </v-card>
</template>
<script>
export default {
  props: {
    product: String,
    price: Number,
    description: String,
  },
};
</script>
