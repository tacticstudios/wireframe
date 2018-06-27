<template lang="pug">
  
#main-menu
    ul
        li(v-for='menu in menus')
            a(v-bind:href='menu.url') {{ menu.text }}

</template>

<script>
export default {
  name: 'main-menu',
  data () {
    return { 
        menus: [
            { url: '#mas_populares', text: 'Mas populares' },
            { url: '#nuevos', text: 'Nuevos' },
            { url: '#mas_valorados', text: 'Mas valorados' },
            { url: '#acerca_de_mi', text: 'Acerca de mi' },
        ]
    }
  }
}
</script>

<style lang="stylus">

#main-menu
    //flex 0 1 500px
    //margin 1rem .25em
    //box-sizing border-box
    //width 18rem
    
ul
    list-style-type none
    padding 0

li
    display inline-block
    margin 0 10px

</style>
