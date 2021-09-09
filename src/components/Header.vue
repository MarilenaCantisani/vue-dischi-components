<template>
  <header>
    <div class="container">
      <!-- Logo -->
      <img id="logo" src="@/assets/logo.png" alt="logo" />
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped lang="scss">
//// Variables
@import "../assets/scss/Generals/Style.scss";
//// Header style
@import "../assets/scss/Header/Header.scss";
</style>