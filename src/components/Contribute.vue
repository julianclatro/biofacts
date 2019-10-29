<template>
  <div id="contribute">
    <div class="ui grid container">
      <div class="eight wide column">
        <div class="firm--petition">
          <div class="box">
            <h1>¿Como podes ayudar?</h1>
            <p>Estamos buscando conseguir 100 mil firmas</p>
            <button class="ui green button firm">
              <img class="button--icon" src="../assets/firm.svg" alt="">
              <div class="button--text">
                Firmá la Petición
              </div>
            </button>
          </div>
        </div>
      </div>
      <div class="eight wide column">
        <img src="../assets/biotag.svg" alt="">
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
  #contribute {
    background: #0165FE;
  }
  .ui.grid.container {
    padding-top: 40px;
    padding-bottom: 40px;
  }
  .character {
    height: 320px;
  }
  h1, p {
    color: white;
  }
  button.button.firm {
    display: inline-flex;
    align-items: center;
    justify-content: center;
  }
  .button--icon {
    height: 32px;
  }
  .button--text {
    padding-left: 8px;
    font-family: 'Poppins', sans-serif;
    font-size: 16px;
    font-weight: 600;
  }
</style>
