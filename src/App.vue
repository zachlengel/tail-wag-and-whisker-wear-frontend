<script>
import Header from "./components/Header.vue";
import Content from "./components/Content.vue";
import Footer from "./components/Footer.vue";
// import logo from "./assets/logo.png";

export default {
  name: "app",
  components: {
    Header,
    Content,
    Footer,
  },
};
</script>

<template>
  <div>
    <Header />
    <!-- <img v-bind:src="logo.png" width="300px" height="300px" /> -->
    <Content />
    <Footer />
  </div>
</template>

<style></style>
