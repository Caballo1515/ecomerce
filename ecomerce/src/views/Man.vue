<template>
  <div class="home">
    <h1>Hello World</h1>
    <v-col>
      <v-row v-for="product in products" :key="product.id">
        <ProductCard
          :description="product.description"
          :price="product.price"
          :product="product.title"
        ></ProductCard>
      </v-row>
    </v-col>
  </div>
</template>

<script>
// @ is an alias to /src
import ProductCard from "../components/ProductCard.vue";
import axios from "axios";

export default {
  name: "Man",
  components: {
    ProductCard,
  },
  data() {
    return {
      products: [],
      productName: "",
      productPice: 0,
      ProductDescription: "",
    };
  },
  created() {
    let vue = this;
    axios.get("https://fakestoreapi.com/products").then(function (response) {
      vue.products = response.data;
    });
  },
};
</script>
