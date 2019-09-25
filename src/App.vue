<template>
  <div id="app">
    <div class="content">
      <Header />
    </div>
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "app",
  components: {
    Header,
    Footer
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
  height: calc(100vh - 186.64px);
}
html,
body,
#app,
.content {
  @extend .max-height;
}
</style>
