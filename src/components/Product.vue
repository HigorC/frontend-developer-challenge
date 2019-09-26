<template>
  <div class="product">
    <img src="//imagens.pontofrio.com.br/Control/ArquivoExibir.aspx?IdArquivo=6584703" alt="aaa" />
    <div class="description">
      <p class="name">Nome</p>
      <p class="about">descricao</p>
      <p class="old-price">De: R$213</p>
      <p class="price">Por: R$ 19,99</p>
      <p class="parcel">ou 4x 9989</p>
    </div>
    <button>Comprar</button>
  </div>
</template>

<script>
export default {
  name: "Product"
};
</script>

<style lang="scss" scoped>
.product {
  height: 350px;
  width: 201px;
  img {
    width: 200px;
    height: 150px;
    border: 1px solid #707070;
  }

  button {
    border-radius: 4px;
    width: 100%;
    border: 1px solid #707070;
    background-color: #FFFFFF;
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