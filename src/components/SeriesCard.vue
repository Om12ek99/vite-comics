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
       margin-bottom: 25px;
        img{
            width: 150px;
            height:150px;
            object-fit:cover;
            cursor: pointer;  
                      
        };

        h4{
            color: aliceblue;
            width:150px;
            font-size: 13px;
            margin-top:15px;   
        }
    }
</style>