<script>
import { store } from "../store";
import CharacterCard from "./CharacterCard.vue";

export default {
    name: "CharactersList",
    data() {
        return {
            store: store,
        }
    },
    components: {
        CharacterCard,
    }
}
</script>


<template>
    <div class="container d-flex flex-wrap justify-content-between p-2">
        <CharacterCard v-for="(card, index) in store.characters" />
    </div>
</template>


<style lang="scss" scoped>

</style>