<template>
  <div class="about">
    <ListProducts :category="'products/category/jewelery'"></ListProducts>
  </div>
</template>
<script>
import ListProducts from '../components/ListProducts.vue'


export default {
  name: "Woman",
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
