<template>
  <div>
    <Hero />
    <Contribute />
    <JoinTheMove />
    <Upcomming />
    <WhoWeAre />
    <Thanks />
  </div>
</template>

<script>
  import Hero from './components/Hero.vue'
  import Contribute from './components/Contribute.vue'
  import WhoWeAre from './components/WhoWeAre.vue'
  import JoinTheMove from './components/JoinTheMove.vue'
  import Upcomming from './components/Upcomming.vue'
  import Thanks from './components/Thanks.vue'

  export default {
    name: 'app',
    components: {
      WhoWeAre,
      Hero,
      Upcomming,
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
  p, .ordered.list .item {
    font-family: 'Open Sans', sans-serif;
    font-size: 17px;
    text-align: justify;
    text-justify: inter-word;
  }
  .grid--right-content {
    padding-left: 20px;
  }
</style>
