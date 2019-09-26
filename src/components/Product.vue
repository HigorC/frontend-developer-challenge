<template>
  <div class="product">
    <img :src="product.image" alt="Image" />
    <div class="description">
      <p class="name">{{product.name}}</p>
      <p class="about">{{product.description}}</p>
      <p class="old-price">De: R${{product.oldPrice}}</p>
      <p class="price">Por: R${{product.price}}</p>
      <p class="parcel">ou {{product.installments.count}}x de R${{product.installments.value}}</p>
    </div>
    <button>Comprar</button>
  </div>
</template>

<script>
export default {
  name: "Product",
  props: {
    product: Object
  }
};
</script>

<style lang="scss" scoped>
.product {
  height: 350px;
  width: 201px;

  display: inline-block;
  margin-bottom: 39px;

  img {
    width: 200px;
    height: 150px;
    border: 1px solid #707070;
  }

  button {
    border-radius: 4px;
    width: 100%;
    border: 1px solid #707070;
    background-color: #ffffff;
    font-size: 16px;
    padding: 6px 0;
    color: #888888;
  }

  .description {
    text-align: left;

    .name {
      font-size: 14px;
      height: 16px;
      padding-bottom: 10px;
    }

    .about {
      font-size: 12px;
      height: 60px;
    }

    .old-price {
      font-size: 12px;
      height: 14px;
      padding-bottom: 6px;
    }

    .price {
      font-size: 16px;
      font-weight: bold;
      height: 19px;
      padding-bottom: 7px;
    }

    .parcel {
      font-size: 12px;
      height: 14px;
      padding-bottom: 10px;
    }
  }
}
</style>