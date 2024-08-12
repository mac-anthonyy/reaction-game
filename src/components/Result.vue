
<template>
  <h4>Your Reaction Time is: {{ score }} ms </h4>
  <p class="rank"> {{ rank }}</p>
</template>

<script>
export default {
    props: ['score'], //to accept the prop "score" that was passed in from App.vue component
    data(){
        return {
            rank: null
        }
    },
    mounted(){
        if (this.score < 250 ){
            this.rank = "Excellent";
        } else if ( this.score < 450 ){
            this.rank = "Nice! Rapid Reflexes"
        }else {
            this.rank = "Slow as snail..."
        }
    }
}
</script>

<style>
    .rank{
        font-size: 1.4em;
        color: #0faf87;
        font-weight: bold;
    }
</style>