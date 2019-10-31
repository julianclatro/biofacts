<template>
  <div>
    <div class="" v-if="!isMobile()">
      <Hero />
      <Contribute />
      <JoinTheMove />
      <Upcomming />
      <WhoWeAre />
      <Thanks />
    </div>
    <div class="" v-if="isMobile()">
      <HeroMobile />
      <ContributeMobile />
      <JoinTheMoveMobile />
      <UpcommingMobile />
      <WhoWeAreMobile />
      <ThanksMobile />
    </div>
  </div>
</template>

<script>
  import Hero from './components/Hero.vue'
  import Contribute from './components/Contribute.vue'
  import WhoWeAre from './components/WhoWeAre.vue'
  import JoinTheMove from './components/JoinTheMove.vue'
  import Upcomming from './components/Upcomming.vue'
  import Thanks from './components/Thanks.vue'

  import HeroMobile from './components/mobile/HeroMobile.vue'
  import ContributeMobile from './components/mobile/ContributeMobile.vue'
  import WhoWeAreMobile from './components/mobile/WhoWeAreMobile.vue'
  import JoinTheMoveMobile from './components/mobile/JoinTheMoveMobile.vue'
  import UpcommingMobile from './components/mobile/UpcommingMobile.vue'
  import ThanksMobile from './components/mobile/ThanksMobile.vue'

  export default {
    name: 'app',
    methods: {
     isMobile() {
       if(/Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent)) {
         return true
       } else {
         return false
       }
     }
    },
    components: {
      WhoWeAre,
      Hero,
      Upcomming,
      Contribute,
      JoinTheMove,
      Thanks,
      WhoWeAreMobile,
      HeroMobile,
      UpcommingMobile,
      ContributeMobile,
      JoinTheMoveMobile,
      ThanksMobile
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
