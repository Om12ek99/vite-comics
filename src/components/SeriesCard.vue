<script>
    export default {
                props: {
                    cardThumb: String,
                    cardPrice: String,
                    cardSeries: String,
                    cardType: String,

                },
        }
</script>

<template>
    <div class="card">
        <img :src= "cardThumb"
             :alt= "cardSeries">
        <h4> {{cardSeries}} </h4>
    </div>
</template>
<style scoped lang="scss">
    .card {
        img{
            width: 80px;
        }
        h4{
            color: aliceblue;
        }
    }
</style>