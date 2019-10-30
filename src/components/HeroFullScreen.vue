<template>
  <div id="hero">
    <div class="fullscreen-bg">
      <video loop muted autoplay poster="img/videoframe.jpg" class="fullscreen-bg__video">
          <source src="../assets/wood.mp4" type="video/mp4">
      </video>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'HeroFullScreen',
    el: '#hero',
  }
</script>

<style scoped>
  #hero {
    height: 50vh;
  }

  .fullscreen-bg {
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
      overflow: hidden;
      z-index: -100;
  }

  .fullscreen-bg__video {
      background-size: cover;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
  }
</style>
