<template>
  <div id="app">
    <!--//// Header -->
    <Header />
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
export default {
  name: "App",
  components: {
    Header,
  },
};
</script>

<style lang="scss">
//// Variables
@import "./assets/scss/Generals/Style.scss";
</style>
