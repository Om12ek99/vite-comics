<script>
    export default{
        data(){
            return{
                images:[
        {
          image: "buy-comics-digital-comics.png",
          title: "DIGITAL COMICS",
        },
        {
          image: "buy-comics-merchandise.png",
          title: "DC MERCHANDISE",
        },
        {
          image: "buy-comics-subscriptions.png",
          title: "SUBSCRIPTION",
        },
        {
          image: "buy-comics-shop-locator.png",
          title: "COMIC SHOP LOCATOR",
        },
        {
          image: "buy-dc-power-visa.svg",
          title: "DC POWER VISA",
        },
          ]
            }
        },

        methods: {

            // funzione per richiamare un immagine dinamica
            getImageUrl(imageName) {
                return new URL(`../assets/img/${imageName}`, import.meta.url).href;
            },
        },
    };
</script>

<template>
    <section>
        <div class="container">
            <ul>
                <li 
                v-for = "CurImage in images">
                    <img :src="getImageUrl(CurImage.image)" alt="">
                    <h4> {{CurImage.title}} </h4>
                </li>
            </ul>
        </div>
    </section>
    
</template>

<style scoped lang="scss">
    @use "../style/partials/variables" as *;
    @use "../style/partials/mixin" as *;

    section {
        background-color: $primary-color;
        padding: 3rem 0;
        color: $white;
        
        ul{
            @include flex(row, space-evenly, center);
            
            li{
                @include flex(row, space-evenly, center);
                gap:0.5rem;
            }
            
            img{
            height:40px;
        }
        h4{
            font-size:0.8rem;
            font-weight:300;
        }
        }
       
    }
</style>