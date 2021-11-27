<template>
  <v-container>
    <v-row v-for="product in products" :key="product.id">
      <v-col>
        <ProductCard
          :description="product.description"
          :price="product.price"
          :product="product.title"
        ></ProductCard>
      </v-col>
    </v-row>
  </v-container>
</template>
<script>
import ProductCard from "../components/ProductCard.vue";
import axios from "axios";

export default {
  name: "ListProducts",
  components: {
    ProductCard,
  },
  data() {
    return {
      products: [],
      productName: "",
      productPice: 0,
      ProductDescription: "",
      urlApi: ""
    };
  },
  mounted() {
    let vue = this;
    this.urlApi = "https://fakestoreapi.com/" + this.category;
    console.log(this.urlApi)
    axios.get(vue.urlApi).then(function (response) {
      vue.products = response.data;
    });
  },
  props: {
    category: String,
  },
};
</script>
<style scoped>
* {
  padding: auto;
  margin: auto;
}
</style>
