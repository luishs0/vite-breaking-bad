<script>
export default {
    name: "CharacterCard",
    data() {
        return {

        }
    }
}
</script>


<template>
    <div class="ms_card mb-3">
        <div class="card-img">
            <img src="https://images.squarespace-cdn.com/content/v1/56a5f5ef5827c35bf58e8e02/1517306531940-MSJ88JW0TQR1WNLNCZK5/Algo_Logo.jpeg"
                alt="">
        </div>

        <div class="card-text text-center">
            <div class="name mt-3 mb-3">Name</div>
            <div class="title mt-1 mb-1">Breaking Bad</div>
            <div class="status mt-1 mb-1">Status</div>
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