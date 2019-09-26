<template>
  <div class="home">
    <p class="title">Sua seleção especial</p>
    <span
      class="products"
      v-for="(product, index) in products"
      :class="{'no-margin': ((index+1) % 4) == 0}"
    >
      <Product :product="product" />

      <br v-if="((index+1) % 4) == 0" />
    </span>

    <button class="btn-more-products" @click="getMoreProducts">Ainda mais produtos aqui!</button>
  </div>
</template>

<script>
import Product from "./Product.vue";

const axios = require("axios");

export default {
  name: "Home",
  data: function() {
    return {
      products: [],
      urlNextRequest:
        "https://frontend-intern-challenge-api.iurykrieger.now.sh/products?page=1"
    };
  },
  components: {
    Product
  },
  methods: {
    getMoreProducts: function() {
      axios.get(this.urlNextRequest).then(res => {
        this.products = this.products.concat(res.data.products);
        this.urlNextRequest = "//" + res.data.nextPage;
        console.log(res);
      });
    }
  },
  created: function() {
      this.getMoreProducts();
  }
};
</script>

<style lang="scss" scoped>
.home {
  text-align: center;
  color: #888888;
  font-size: 18px;
  padding: 48.67px 0 50px 0;

  .title {
    padding-bottom: 50px;
    font-size: 18px;
    font-weight: bold;
  }

  .products {
    margin-right: 41px;
  }

  .no-margin {
    margin-right: 0;
  }

  .btn-more-products {
    width: 260px;
    height: 39px;
    border: 1px solid #707070;
    color: #888888;
    border-radius: 4px;
    background-color: #ffffff;
    font-size: 16px;
  }
}
</style>