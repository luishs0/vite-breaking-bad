<script>
import axios from "axios";
import CharactersList from "./components/CharactersList.vue";
import { store } from "./store";

export default {
  data() {
    return {
      store,
    }
  },
  components: {
    CharactersList
  },
  created() {
    this.getCharacters();
  },
  methods: {
    getCharacters() {
      let apiUrl = "";
      if (this.store.selected === "Breaking Bad") {
        apiUrl = "https://www.breakingbadapi.com/api/characters?category=Breaking+Bad";
      } else if (this.store.selected === "Better Call Saul") {
        apiUrl = "https://www.breakingbadapi.com/api/characters?category=Better+Call+Saul";
      } else {
        apiUrl = "https://www.breakingbadapi.com/api/characters";
      }

      axios.get(apiUrl).then((resp) => {
        this.store.characters = resp.data;
        console.log(this.store.characters);
      });


    }
  }
}

</script>


<template>
  <div class="container pt-3 pb-3">
    <select name="select" id="select" v-model="store.selected">
      <option value="" selected>All</option>
      <option value="Breaking Bad">Breaking Bad</option>
      <option value="Better Call Saul">Better Call Saul</option>
    </select>
    <button class="btn btn-primary" @click="getCharacters">Search</button>
  </div>
  <CharactersList />
</template>


<style lang="scss">
@use "./styles/general.scss" as *;
</style>
