<template>
  <!--* Card -->
  <li class="card">
    <img class="poster" src="@/assets/demo.jpg" alt="card-title" />
    <h2 class="title text-uppercase">titolo</h2>
    <address class="author text-capitalize text-normal">autore</address>
    <time class="year text-grey">anno</time>
  </li>
</template>

<script>
export default {
  name: "Card",
};
</script>

<style scoped lang="scss">
//// Variables
@import "../assets/scss/Generals/Style.scss";

//// Card style
.card {
  text-align: center;
  list-style-type: none;
  padding: 20px;
  width: 200px;
  background-color: $light-blue;
  margin: 10px 10px;
  .poster {
    width: 100%;
    height: auto;
  }
  .title {
    padding: 15px 0;
    font-size: 22px;
    color: $white;
  }
  .author {
    font-size: 20px;
    padding-top: 15px;
    color: $light-grey;
  }
  .year {
    font-size: 15px;
    color: $light-grey;
  }
}
</style>