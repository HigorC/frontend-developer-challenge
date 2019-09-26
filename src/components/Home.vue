<template>
  <div class="home">
    <p class="title">Sua seleção especial</p>

    <Product/>
  </div>
</template>

<script>
import Product from "./Product.vue";

export default {
  name: "Home",
  components: {
    Product
  }
};
</script>

<style lang="scss" scoped>
.home {
  text-align: center;
  color: #888888;
  font-size: 18px;
  padding: 48.67px 0 50px 0;
  height: 22px;

  .title{
      padding-bottom: 50px;
  }
}
</style>