<template>
  <main>
    <article>
      <!-- CARD SECTION -->
      <ul class="card-section">
        <Card />
      </ul>
    </article>
  </main>
</template>

<script>
import Card from "../components/Card.vue";
export default {
  name: "Main",
  components: {
    Card,
  },
};
</script>

<style scoped lang="scss">
//// Variables
@import "../assets/scss/Generals/Style.scss";
//// Card section style
.card-section {
  margin-top: 50px;
  padding: 0 10px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
</style>