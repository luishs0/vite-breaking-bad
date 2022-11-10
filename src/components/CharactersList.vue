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

</template>


<style lang="scss" scoped>

</style>