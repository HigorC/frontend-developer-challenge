<template>
  <div class="header">
    <div class="title">
      <p class="sub">uma seleção de produtos</p>
      <p class="principal">especial para você</p>
      <p
        class="phrase"
      >Todos os produtos desta lista foram selecionados a partir da sua navegação. Aproveite!</p>
    </div>

    <div class="buttons">
      <button>Conheça a Linx</button>
      <button>Ajude o algorítimo</button>
      <button>Seus produtos</button>
      <button>Compartilhe</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header"
};
</script>

<style lang="scss" scoped>
.header {
  text-align: center;
  font-family: "Helvetica" !important;
  max-height: 319.33px;
  min-height: 319.33px;
  background-color: #707070;
  color: #ffffff;

  .title {
    .sub {
      padding-top: 69px;
      font-size: 20px;
      height: 23px;
    }

    .principal {
      font-size: 40px;
      height: 48px;
      font-weight: bold;
    }

    .phrase {
      font-size: 14px;
      height: 16px;
      padding: 24px 0 50px 0;
    }
  }

  .buttons {
    padding-bottom: 61px;

    button {
      min-height: 40px;
      max-height: 40px;
      min-width: 160px;
      max-width: 160px;
      background-color: #ffffff;
      border: 1px solid #707070;
      border-radius: 4px;
      color: #888888;
      margin-right: 40px;
      font-family: 'Helvetica';
      font-size: 16px;
    }

    button:last-child {
      margin-right: 0;
    }
  }
}
</style>
