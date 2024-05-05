<script>
    export default {
        data (){
            return {
                navArray: [
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
                    
                    
                ]
            }
        }
    }
</script>

<template>
    <header>
        <div class="container">
            <div class="logo">
                <img 
                src="../assets/img/dc-logo.png" 
                alt="Logo DC">
            </div>
                <div class="navbar">
                    <ul>
                        <li 
                        v-for = "(CurListItem, index) in navArray" 
                        :class = "{active: CurListItem.isActive}"> 
                            <a href="#">
                            {{CurListItem.title}}
                            </a>                    
                        </li>
                    </ul>
                </div>        
            </div>
        
    </header>
</template>

<style scoped lang="scss">
    @use "../style/partials/mixin" as *;
    @use "../style/partials/variables" as *;
    .container {
        height: 100px;
        /* debug */
        background-color: $white;            
        margin-bottom: 0;
        @include flex(row, space-between, center );

        /* image style */
        img {
            height: 75px;
            width: 75px;
            
        }

        /* navigation links styles */
        ul {
            @include flex(row, space-evenly, center);
            gap: 2rem;
            font-size: smaller;
            margin-right:3rem;              /*non so perche ma non me lo ha centrato nel container*/
           

            li {
                &.active {
                    color: $primary-color;
                }
            }
        }
    }
</style>
