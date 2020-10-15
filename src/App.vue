<template>
  <div class="Spotify">
    <Navbar />
    <Home />
    <Player />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Navbar from './components/Navbar.vue'
import Player from './components/Player.vue'
import Home from './components/Home.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    Navbar,
    Player,
    Home
  }
}
</script>

<style lang="scss">
* {
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
  font-family: 'Montserrat', sans-serif;
}

.Spotify {
  position: relative;
  padding: 0 0 90px 230px;
}
</style>
