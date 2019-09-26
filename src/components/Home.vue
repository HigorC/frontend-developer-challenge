<template>
  <div class="home">
    <p class="title">Sua seleção especial</p>
    <span class="products" v-for="(product, index) in products" :class="{'no-margin': ((index+1) % 4) == 0}">
      <Product :product="product" />

      <br v-if="((index+1) % 4) == 0" />
    </span>
    <div class="clear"></div>
  </div>
</template>

<script>
import Product from "./Product.vue";

const axios = require("axios");

export default {
  name: "Home",
  data: function() {
    return {
      products: []
    };
  },
  components: {
    Product
  },
  created: function() {
    axios
      .get(
        "https://frontend-intern-challenge-api.iurykrieger.now.sh/products?page=1"
      )
      .then(res => {
        this.products = res.data.products;
        console.log(res);
      });
  }
};
</script>

<style lang="scss" scoped>
.home {
  text-align: center;
  color: #888888;
  font-size: 18px;
  padding: 48.67px 0 50px 0;
  //   height: 22px;

  .title {
    padding-bottom: 50px;
  }

  .products {
    // float: right;
    margin-right: 41px;
    
  }

  .no-margin{
        margin-right: 0;
    }

  .clear {
    //   clear: both;
  }
}
</style>