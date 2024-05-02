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
        <div class="logo">
            <img src="../assets/img/dc-logo.png" alt="">
        </div>
        <div class="navbar">
            <ul>
                <li v-for = "(CurListItem, index) in navArray">
                    {{CurListItem}}
                </li>
            </ul>
        </div>
    </header>
</template>

<style scoped lang="scss">
</style>
