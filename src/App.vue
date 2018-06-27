<template lang="pug">
  
#app
  header
    //Navbar component
    nav-bar
  br

  //MainMenu component
  main-menu
  
  br
  .centered
    card(v-for='item in items', :title='item.title', :text='item.text')
  
  //
    span(v-for='n in 16')
      //Card component
      card
  |

</template>

<script>
import Card from './Card.vue'
import MainMenu from './MainMenu.vue'
import Navbar from './Navbar.vue'

export default {
  name: 'app',
  components: {
    //a agregar: MainMenu, Navbar
    'card': Card,
    'main-menu': MainMenu,
    'nav-bar': Navbar
  },
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      items: [
          { title: 'Titulo 1', text: 'Texto 1 Texto 1 Texto 1 Texto 1 Texto 1 Texto 1 Texto 1 Texto 1 ' },
          { title: 'Titulo 2', text: 'Texto 2 Texto 2 Texto 2 Texto 2 Texto 2 Texto 2 Texto 2 Texto 2 ' },
          { title: 'Titulo 3', text: 'Texto 3 Texto 3 Texto 3 Texto 3 Texto 3 Texto 3 Texto 3 Texto 3 ' },
          { title: 'Titulo 4', text: 'Texto 4 Texto 4 Texto 4 Texto 4 Texto 4 Texto 4 Texto 4 Texto 4 ' },
          { title: 'Titulo 5', text: 'Texto 5 Texto 5 Texto 5 Texto 5 Texto 5 Texto 5 Texto 5 Texto 5 ' },
          { title: 'Titulo 6', text: 'Texto 6 Texto 6 Texto 6 Texto 6 Texto 6 Texto 6 Texto 6 Texto 6 ' },
          { title: 'Titulo 7', text: 'Texto 7 Texto 7 Texto 7 Texto 7 Texto 7 Texto 7 Texto 7 Texto 7 ' },
          { title: 'Titulo 8', text: 'Texto 8 Texto 8 Texto 8 Texto 8 Texto 8 Texto 8 Texto 8 Texto 8 ' }
      ]
    }
  }
}
</script>

<style lang="stylus">
#app
    font-family 'Avenir', Helvetica, Arial, sans-serif
    -webkit-font-smoothing antialiased
    -moz-osx-font-smoothing grayscale
    text-align center
    color #2c3e50
    //margin-top 60px
    margin 0 1em

.centered
    margin-left 2em
    margin-right 2em
    display flex
    flex-wrap wrap
    justify-content space-between

h1
    font-weight normal
    font-size 18px

h2
    font-weight normal

//ul li

a
    color black//#42b983

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
