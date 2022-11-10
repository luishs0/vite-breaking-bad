<script>
export default {
    name: "CharacterCard",
    data() {
        return {

        }
    },
    props: {
        img: String,
        name: String,
        status: String
    }
}
</script>


<template>
    <div class="ms_card mb-3 d-flex flex-column justify-content-between">
        <div class="card-img">
            <img :src="img" :alt="name">
        </div>

        <div class="card-text text-center">
            <div class="name">{{ name }}</div>
            <div class="status">{{ status }}</div>
            <div class="title">Breaking Bad</div>
        </div>
    </div>
</template>


<style lang="scss" scoped>
.ms_card {
    width: calc(100% / 5 - 1rem);
    background-color: #707070;
}

.card-img {
    width: 100%;
    height: 70%;
}

.card-text {
    height: 30%;
    padding: 1rem;
}

.name {
    color: white;
}

.title,
.status {
    color: #cfcfcf;
}

img {
    padding: .5rem;
}
</style>