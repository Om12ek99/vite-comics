<script>
    export default {
        data (){
            return {
                navArray: [
                    "CHARACTERS",
                    "COMICS",
                    "MOVIES",
                    "TV",
                    "GAMES",
                    "COLLECTIBLES",
                    "VIDEOS",
                    "FANS",
                    "NEWS",
                    "SHOP"
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
                        v-for = "(CurListItem, index) in navArray"> 
                            <a href="#">
                            {{CurListItem}}
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
        background-color: white;            /*da cambiare*/
        margin-bottom: 0;
        @include flex(row, space-between, center );

        /* image style */
        img {
            height: 75px;
            width: 75px;
            margin-left: 5rem;
        }

        /* navigation links styles */
        ul {
            @include flex(row, space-evenly, center );
            gap: 2rem;
            font-size: smaller;
            margin-right: 5rem;
        }
    }
</style>
