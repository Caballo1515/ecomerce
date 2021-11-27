<template>
  <div class="home">
    <ListProducts :category="'products/category/electronics'"></ListProducts>
  </div>
</template>

<script>

import ListProducts from '../components/ListProducts.vue'


export default {
  name: "Man",
  components: {
    ListProducts,
  },
  data() {
    return {
      category: '',
    };
  },

};
</script>
<style scoped>
.home{
  margin: auto;
  padding: auto;
  width: 50%;
}
</style>
