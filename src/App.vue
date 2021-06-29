<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <Game/>
</template>

<script>
    import Game from './components/Game.vue'

export default {
  name: 'App',
  components: {
      Game
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

img{

    max-width: 150px;
    max-height: 150px;
    border-radius: 200px;
    box-shadow: 0px 0px 25px rgba(0,0,0,0.5);

}
</style>
