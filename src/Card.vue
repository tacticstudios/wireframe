<template lang="pug">
  
#card
    .card-body
        .card-title {{title}}
        .card-text {{text}}

</template>

<script>
export default {
  name: 'card',
  props: ['title', 'text']
}
</script>

<style lang="stylus">

#card
    flex 0 1 500px
    margin 1rem .25em
    box-sizing border-box
    width 18rem
    
.card-body
    //flex 0 1 500px
    //margin 1rem .25em
    //box-sizing border-box
    //width 18rem

    border-radius 20px 20px 20px 20px
    background-color lightgrey

.card-title
    font-size 16px

.card-text
    font-size 12px

@media screen and (max-width: 40em)
    .cards
        display flex
        flex-wrap wrap
        justify-content space-between
    #card
        flex 0 1 calc(100% - 1em)

@media screen and (min-width: 40em)
    .cards
        display flex
        flex-wrap wrap
        justify-content space-between
    #card
        flex 0 1 calc(50% - 1em)
        //box-sizing

@media screen and (min-width: 60em) {
    #card {
        flex 0 1 calc(25% - 1em)
    }
}

</style>
