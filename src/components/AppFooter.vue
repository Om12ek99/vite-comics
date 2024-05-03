<script>
    export default{
        data(){
            return {
                dcComicsArray: [
                    {
                        title:"CHARACTERS",
                        isActive: false,
                    },
                    {
                        title:"COMICS",
                        isActive: false,
                    },
                    {
                        title:"MOVIES",
                        isActive: false,
                    },
                    {
                        title:"TV",
                        isActive: false,
                    },
                    {
                        title:"GAMES",
                        isActive: true,
                    },
                    {
                        title:"COLLECTIBLES",
                        isActive: false,
                    },
                    {
                        title:"FANS",
                        isActive: false,
                    },
                    {
                        title:"NEWS",
                        isActive: false,
                    },
                    {
                        title:"SHOP",
                        isActive: false,
                    },                   
                    
                    
                ],
                shopArray: [
                    {
                        title:"Shop DC",
                        isActive: false,
                    },  
                    {
                        title:"Shop DC collectibles",
                        isActive: false,
                    },  
                    
                ],
                dcArray:[
                    {
                        title:"Terms of use",
                        isActive: false,
                    },  
                    {
                        title:"Privacy policy (New)",
                        isActive: false,
                    },  
                    {
                        title:"Ad Choices",
                        isActive: false,
                    },  
                    {
                        title:"Advertising",
                        isActive: false,
                    },  
                    {
                        title:"Jobs",
                        isActive: false,
                    }, 
                    {
                        title:"Subscription",
                        isActive: false,
                    },   
                    {
                        title:"Talent Workshop",
                        isActive: false,
                    },  
                    {
                        title:"CPSC Certificate",
                        isActive: false,
                    },  
                    {
                        title:"Ratings",
                        isActive: false,
                    },  
                    {
                        title:"Shop Help",
                        isActive: false,
                    },  
                    {
                        title:"Contact Us",
                        isActive: false,
                    },  
                ],
                sitesArray:[
                    {
                        title:"DC",
                        isActive: false,
                    },  
                    {
                        title:"MAD magazine",
                        isActive: false,
                    },  
                    {
                        title:"DC Kids",
                        isActive: false,
                    },  
                    {
                        title:"DC Universe",
                        isActive: false,
                    },  
                    {
                        title:"Dc Power Visa",
                        isActive: false,
                    },  
                ]
            }
        }
    }
</script>

<template>
    <footer>
    <div class="container">
        <div class="links">
            <!-- first column -->
            <div class="col">
                <!-- DC comics -->
                <div class="section">
                    <h1>DC COMICS</h1>
                    <ul>
                        <li 
                        v-for="curLink in dcComicsArray">
                            {{curLink.title}}
                        </li>
                    </ul>
                </div>
                <!-- Shop -->
                <div class="section">
                    <h1>SHOP</h1>
                    <ul>
                        <li 
                        v-for="curLink in shopArray">
                            {{curLink.title}}
                        </li>
                    </ul>
                </div>
            </div>
            <!-- second column -->
            <div class="col">
                <div class="section">
                    <h1>DC</h1>
                    <ul>
                        <li 
                        v-for="curLink in dcArray">
                            {{curLink.title}}
                        </li>
                    </ul>
                </div>
            </div>
            <div class="col">
                <div class="section">
                    <h1>SITES</h1>
                    <ul>
                        <li 
                        v-for="curLink in sitesArray">
                            {{curLink.title}}
                        </li>
                    </ul>
                </div>
            </div>

        </div>
    </div>
</footer>
</template>

<style scoped lang="scss">
    @use "../style/partials/mixin" as *;
    @use "../style/partials/variables" as *;
    
    footer{
        background-image: url(../assets/img/footer-bg.jpg);
        padding: 1rem 1rem;
        height:fit-content;
    

        .links{
            @include flex(row, flex-start,start );
            gap: 3rem;
            .col{
                @include flex(column, flex-start,start );
                gap:0.8rem;
                .section{
                    @include flex(column, flex-start,start );
                    gap:0.8rem;
                }
            }
            h1{
                color: $white;
                font-size: 1rem;
            }

            ul{
                @include flex(column, flex-start,start );
                gap:0.5rem;
                li {              
                color: $grey;
                font-size:0.6rem;
                }
            }
            
        }
    }

</style>