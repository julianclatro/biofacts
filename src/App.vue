<template>
  <div>
    <Hero />
    <Contribute />
    <JoinTheMove />
    <BioFacts />
    <Thanks />
  </div>
</template>

<script>
  import Hero from './components/Hero.vue'
  import Contribute from './components/Contribute.vue'
  import BioFacts from './components/BioFacts.vue'
  import JoinTheMove from './components/JoinTheMove.vue'
  import Thanks from './components/Thanks.vue'

  export default {
    name: 'app',
    components: {
      BioFacts,
      Hero,
      Contribute,
      JoinTheMove,
      Thanks
    }
  }
</script>

<style>
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }
</style>
