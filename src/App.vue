<template>
  <div id="app">
    <div class="content">
      <Header />
      <Home />
    </div>
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Home from "./components/Home.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "app",
  components: {
    Header,
    Home,
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
body {
  @extend .max-height;
}

button {
  cursor: pointer;
  transition: 0.2s all;
  &:hover {
    background-color: #86c0e6 !important;
    color: #ffffff !important;
    text-shadow: 0px 0px 3px #000000;
  }
}
</style>
