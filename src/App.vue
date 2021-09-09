<template>
  <div id="app">
    <!--//// Header -->
    <header>
      <div class="container">
        <!-- Logo -->
        <img id="logo" src="@/assets/logo.png" alt="logo" />
        <Search :cards="cards" @changeGenre="search" />
      </div>
    </header>
    <!--//// Main -->
    <Main :cards="cards" />
  </div>
</template>

<script>
import axios from "axios";
import Search from "@/components/Search.vue";
import Main from "@/components/Main.vue";

export default {
  name: "App",
  components: {
    Search,
    Main,
  },
  data() {
    return {
      cards: [],
      selectedGenre: "",
    };
  },
  methods: {
    search(genre) {
      this.selectedGenre = genre;
    },
  },
  computed: {
    // filterGenre() {
    //   return this.cards.filter((card) => {
    //     card.genre.includes(this.selectedGenre);
    //   });
    // },
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

<style lang="scss">
//// Variables
@import "./assets/scss/Generals/Style.scss";
//// Header style
@import "./assets/scss/Header/Header.scss";
</style>
