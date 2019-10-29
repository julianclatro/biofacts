<template>
  <div id="thanks">
    <div class="footer--content">
      <div class="content">
        <a href="#">
          Powered By Eco House
        </a>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Thanks',
    el: '#thanks',
  }
</script>

<style scoped>
  #thanks {
    margin-top: 40px;
    background: black;
    height: 80px;
  }
  .footer--content {
    display: flex;
    align-items: center;
    justify-content: center;
  }
  .content {
    padding-top: 28px;
  }
  a {
    color: white;
  }
</style>
