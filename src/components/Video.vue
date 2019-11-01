<template>
  <div id="video">
    <iframe class="iframe-round" src="https://www.youtube.com/embed/lIb-M4rS6pk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </div>
</template>

<script>
  export default {
    name: 'Video',
    el: '#video'
  }
</script>

<style scoped>
  #video {

  }

  .iframe-round {
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      z-index: 10;
      width: 100%;
      height: 320px;
      border: 0;
      -webkit-border-radius: 20px;
      border-radius: 20px;
  }
</style>
