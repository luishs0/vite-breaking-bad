<script>
import axios from "axios";
import CharactersList from "./components/CharactersList.vue";
import { store } from "./store";

export default {
  data() {
    return {
      store
    }
  },
  components: {
    CharactersList
  },
  created() {
    axios.get("https://www.breakingbadapi.com/api/characters").then((resp) => {
      this.store.characters = resp.data.results;
      console.log(this.store.characters);
    });
  }
}

</script>


<template>

</template>


<style lang="scss">
@use "./styles/general.scss" as *;
</style>
