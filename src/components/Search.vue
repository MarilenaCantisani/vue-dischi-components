<template>
  <select
    class="search"
    v-model.trim="selectGenre"
    @change="$emit('changeGenre', selectGenre)"
  >
    <option>Seleziona un genere</option>
    <option>Rock</option>
    <option>Pop</option>
    <option>Metal</option>
    <option>Jazz</option>
  </select>
</template>

<script>
export default {
  name: "Search",
  props: ["cards"],
  data() {
    return {
      selectGenre: "Seleziona un genere",
    };
  },
};
</script>

<style>
</style>