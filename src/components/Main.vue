<template>
  <main>
    <article>
      <!-- CARD SECTION -->
      <ul class="card-section">
        <li class="card" v-for="(card, index) in cards" :key="index">
          <a href="#"> <Card :card="card" /> </a>
        </li>
      </ul>
    </article>
  </main>
</template>

<script>
import axios from "axios";
import Card from "@/components/Card.vue";
export default {
  name: "Main",
  components: {
    Card,
  },
  data() {
    return {
      cards: [],
    };
  },
  created() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((res) => {
        this.cards = res.data.response;
      });
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
//// Card style
.card {
  text-align: center;
  list-style-type: none;
  padding: 20px;
  width: 220px;
  background-color: $light-blue;
  margin: 10px 10px;
  a {
    text-decoration: none;
  }
}
</style>