<template lang="pug">

#nav-bar
  ul
    li
      a(href="#")
        img(id="imagen" src='./assets/logo.png')

    li(v-for='item in items')
      a(v-bind:href='item.url') {{ item.text }}

</template>

<script>
export default {
  name: 'nav-bar',
  data () {
    return {
      items: [
            { url: '#buscar', text: 'Buscar' },
            { url: '#crear_warique', text: 'Crear Warique' },
            { url: '#login', text: 'Login' },
        ]
    }
  }
}
</script>

<style lang="stylus">

#nav-bar
    background-color lightgrey
    border-radius 10px 10px 10px 10px

#imagen
    height 15%
    width 15%

</style>
