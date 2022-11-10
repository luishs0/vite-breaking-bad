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
    <div class="ms_card">
        <div class="card-img">
            <img src="https://images.squarespace-cdn.com/content/v1/56a5f5ef5827c35bf58e8e02/1517306531940-MSJ88JW0TQR1WNLNCZK5/Algo_Logo.jpeg"
                alt="">
        </div>

        <div class="card-text">
            Algo
        </div>
    </div>
</template>


<style lang="scss" scoped>
.ms_card {
    width: calc(100% / 5 - 1rem);
}

.card-img {
    width: 100%;
}
</style>