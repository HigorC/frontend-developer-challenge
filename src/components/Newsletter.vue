<template>
  <div>
    <p class="title">Compartilhe a novidade</p>
    <p
      class="phrase"
    >Quer que seus amigos também ganhem a lista personalizada deles? Preencha agora!</p>
    <form onsubmit="alert('Enviando email... ou não.');return false">
      <div class="inputs">
        <div class="name">
          <label for="name">Nome do seu amigo:</label>
          <br />
          <input id="name" type="text" required />
        </div>

        <div class="email">
          <label for="email">E-mail:</label>
          <br />
          <input id="email" type="email" required />
        </div>
      </div>

      <button class="enviar">Enviar agora</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "Newsletter"
};
</script>

<style lang="scss" scoped>
.title {
  font-size: 18px;
  font-weight: bold;
  height: 22px;
  margin-bottom: 44px;
}

.phrase {
  font-size: 14px;
  margin-bottom: 39px;
}

.inputs {
  font-size: 12px;
  text-align: center;

  .name,
  .email {
    display: inline-block;
    text-align: left;
  }

  .name {
    margin-right: 40px;
  }

  input {
    margin-top: 7px;
    width: 340px;
    height: 30px;
  }
}

.enviar {
  margin-top: 50px;
  font-size: 16px;
  background-color: #ffffff;
  color: #888888;
  border: 1px solid #707070;
  border-radius: 4px;
  width: 260px;
  height: 39px;
  padding: 11px 0;
  margin-bottom: 142.36px;
}
</style>