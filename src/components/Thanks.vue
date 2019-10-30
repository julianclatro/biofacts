<template>
  <div id="thanks">
    <div class="ui container">
      <div class="content">
        <a href="#">
          En colaboración con
        </a>
        <a href="https://laninia.com/site/">La Niña, </a>
        <a href="https://facebook.com">Facebook y </a>
        <a href="http://www.hacksur.com">Julián Clatro</a>
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
  .content {
    padding-top: 28px;
    float: right;
  }
  a {
    color: white;
  }
</style>
