<template>
  <div id="app">
    <Header />
  </div>
</template>

<script>
import Header from "./components/Header.vue";

export default {
  name: "app",
  components: {
    Header
  }
};
</script>

<style lang="scss">
@import "node_modules/reset-css/sass/_reset";

body {
  margin: 0;
}

html {
  font-family: "Helvetica" !important;
}
.max-height {
  height: calc(100vh - 28px);
}
html,
body,
#app {
  @extend .max-height;
}
</style>
