<script >
  export default {         //aggiungo
    data(){
        return {
            
        }
    }
}
</script>

<template>
  
    <div class="content-section">
        <h1> --> CONTENT GOES HERE <-- </h1>
    </div>
</template>

<style lang = "scss"> 
    @use "../style/partials/mixin" as *;
    .content-section {
        height: 100px;
        margin-top: 0;
        display: inline-block;
        width: 100%;
        /* debug */
        background-color: rgb(0, 0, 0);
        @include flex(row, flex-start, center);
        h1 {
            
            color: rgb(255, 255, 255);     /*da cambiare*/
            font-size: 1rem;
            margin-left: 5rem;
            
        }
    }

</style>
