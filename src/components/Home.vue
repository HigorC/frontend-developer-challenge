<template>
  <div class="home">
    <p class="title">Sua seleção especial</p>

    <transition-group name="fade">
      <span
        class="products"
        v-for="(product, index) in products"
        :key="product"
        :class="{'no-margin': ((index+1) % 4) == 0}"
      >
        <Product :product="product" />

        <br v-if="((index+1) % 4) == 0" />
      </span>
    </transition-group>

    <button class="btn-more-products" @click="getMoreProducts">Ainda mais produtos aqui!</button>
    <Newsletter />
  </div>
</template>

<script>
import Product from "./Product.vue";
import Newsletter from "./Newsletter.vue";

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
    Product,
    Newsletter
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
  padding-top: 48.67px;

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
    margin-bottom: 164px;
  }

  .fade-enter-active,
  .fade-leave-active {
    transition: opacity 0.5s;
  }
  .fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
    opacity: 0;
  }
}
</style>