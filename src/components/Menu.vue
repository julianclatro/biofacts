<template>
  <div class="ui top fixed menu">
    <div class="ui container">
      <img src="../assets/logo.svg" class="ui small image" alt="biofacts">
      <div class="ui secondary right menu">
        <div class="item">
          <a class="" href="https://www.instagram.com/eco.house/">
            <img src="../assets/instagram.svg" alt="" class="ui image social--icon">
          </a>
          <a class="" href="https://www.facebook.com/ecohousee">
            <img src="../assets/facebook.svg" alt="" class="ui image social--icon">
          </a>
          <a class="" href="https://twitter.com/ecohouseok">
            <img src="../assets/twitter.svg" alt="" class="ui image social--icon">
          </a>
          <a class="" href="https://www.youtube.com/channel/UCLdMvgCeKje_BN6JsBa1YGQ">
            <img src="../assets/youtube.svg" alt="" class="ui image social--icon">
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Contribute',
    el: '#contribute',
  }
</script>

<style scoped>
  .secondary.menu.menu a.item {
    font-family: 'Montserrat', sans-serif;
    font-size: 18px;
    font-weight: 600;
  }
  .secondary.menu a.item:hover {
  }

  .social--icon {
    height: 32px;
    margin-left: 8px;
  }

  .menu .container {
    padding-top: 8px;
    padding-bottom: 8px;
  }
</style>
