<template>
  <!--* Card -->
  <div>
    <img class="poster" :src="card.poster" :alt="card.title" />
    <h2 class="title text-uppercase">{{ card.title }}</h2>
    <address class="author text-capitalize text-normal">
      {{ card.author }}
    </address>
    <time :data="card.year" class="year">{{ card.year }}</time>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: ["card"],
};
</script>

<style scoped lang="scss">
//// Variables
@import "../assets/scss/Generals/Style.scss";

//// Card style
.poster {
  width: 100%;
  height: auto;
}
.title {
  padding: 15px 0;
  font-size: 18px;
  color: $white;
}
.author {
  font-size: 16px;
  padding-top: 15px;
  color: $light-grey;
}
.year {
  font-size: 15px;
  color: $light-grey;
}
</style>