<template>
  <div id="contribute">
    <div class="ui grid container">
      <div class="eight wide column">
        <div class="firm--petition">
          <div class="box">
            <h1>Petición en Change.org</h1>
            <p>Objetivo: ¡<b>100 000</b>  firmas! ¡AYUDANOS POR FAVOR!</p>
            <a href="http://www.change.org/infoambiental">
              <button class="ui white large button firm">
                <img class="button--icon" src="../assets/firm.svg" alt="">
                <div class="button--text">
                  Firmá la Petición
                </div>
              </button>
            </a>
            <p class="disclaimer">Cuantos más seamos los que apoyamos la campaña, más ganas de participar tendrán los polítcos y las empresas.</p>
          </div>
        </div>
      </div>
      <div class="right floated eight wide column">
        <div class="grid--right-content">
          <div class="ui basic padded segment">
            <img src="../assets/biowhite_tag.svg" alt="" class="ui image">
          </div>
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
  #contribute {
    background: #09433B;
  }
  .ui.grid.container {
    padding-top: 30px;
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
    background: white;
  }
  .button--icon {
    height: 40px;
  }
  .disclaimer {
    margin-top: 16px;
  }
  .button--text {
    padding-left: 8px;
    color: #09433B;
    font-family: 'Montserrat', sans-serif;
    font-size: 18px;
    font-weight: 600;
  }
</style>
