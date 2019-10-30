<template>
  <div id="biolabels" class="ui container">
    <h1>Calculadora de Materiales</h1>
    <div class="ui grid">
      <div class="three wide column">
        <div>
            <h3 class="ui header">
            Elije un material a continuación:
            </h3>
            <div class="radio-toolbar">
              <input type="radio" v-model="categories" id="radioTodos" value="" checked />
              <label for="radioTodos" class="ui green button">Todos</label>
              <input type="radio" v-model="categories" id="radioAluminio" value="aluminio"/>
              <label for="radioAluminio" class="ui green button">Aluminio</label>
              <input type="radio" v-model="categories" id="radioPlastico" value="plastico"/>
              <label for="radioPlastico" class="ui green button">Plastico</label>
              <input type="radio" v-model="categories" id="radioPet" value="pet"/>
              <label for="radioPet" class="ui green button">Pet</label>
              <input type="radio" v-model="categories" id="radioVidrio" value="vidrio"/>
              <label for="radioVidrio" class="ui green button">Vidrio</label>
              <input type="radio" v-model="categories" id="radioPolipropileno" value="polipropileno"/>
              <label for="radioPolipropileno" class="ui green button">Polipropileno</label>
              <input type="radio" v-model="categories" id="radioCarton" value="carton"/>
              <label for="radioCarton" class="ui green button">Carton</label>
            </div>
        </div>
      </div>
      <div class="thirteen wide column">
        <div class="ui three stackable cards">
          <div class="card biocard" v-for="(product, index) in computedProducts" :key="index">
              <div class="content">
                <div class="content--tag">
                  <div class="content--tag-logo">
                    <img src="../assets/biofacts-01.svg" alt="" class="ui small image">
                  </div>
                  <div class="content--tag-facts">
                    <div class="item">
                      <h4 class="ui header">{{product.name}}</h4>
                    </div>
                    <div class="item fact--years">
                      <h4 class="ui header">{{product.year}} años</h4>
                    </div>
                  </div>
                </div>
              </div>
          </div>
        </div>
      </div>
      </div>
    </div>
</template>

<script>
// import Paginate from 'vuejs-paginate'
// Vue.component('paginate', Paginate)
export default {
  name: 'BioLabels',
  el: '#biolabels',
  data() {
    return {
      categories: [ ],
      years: [ ],
      products: [
        {name:'Encendedor', year:'100', category:'acero+plastico' },
        {name:'Latas', year:'200', category:'aluminio' },
        {name:'Envases', year:'10', category:'aluminio+recubierto' },
        {name:'Caja de Arroz', year:'1', category:'carton+reciclado' },
        {name:'Tuvo de Papas fritas', year:'200', category:'carton+plastico+aluminio' },
        {name:'Botella', year:'4000', category:'vidrio' },
        {name:'Latas de Conserva', year:'60', category:'ojalata' },
        {name:'Envoltura de Manteca', year:'25', category:'laminado+multicapa' },
        {name:'Paquete de Harina', year:'1', category:'papel' },
        {name:'Aljafor', year:'500', category:'papel+aluminio' },
        {name:'Tetrabrik', year:'30', category:'tetrabrik' },
        {name:'Gaseosa', year:'500', category:'pet' },
        {name:'Papel Film', year:'1000', category:'pvc' }
      ],
      sortBy: 'name'
    }
  },
  computed: {
    computedProducts: function () {
      return this.products.filter((item) => {
        // console.log(item.category)
        // console.log(this.years)
        // console.log(this.categories.includes(item.category))
        return (this.categories.length === 0 || this.categories.includes(item.category))
        // return (this.years.length === 0 || this.years.includes(item.year))
      }).sort((a, b) => {
        return a[this.sortBy].toString().localeCompare(b[this.sortBy].toString())
      })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#biolabels {
  padding-top: 80px;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 8px;
}
a {
  color: white;
}
.radio-toolbar input[type="radio"] {
  opacity: 0;
  position: fixed;
  width: 0;
}
.fact--years {
  padding-top: 4px;
}
.radio-toolbar label {
    display: block;
    color: white;
    background-color: #7DA471;
    padding: 12px 12px 8px 12px;
    margin: 4px;
    font-family: 'Poppins', sans-serif;
    font-size: 16px;
    font-weight: 600;
    border: 1px solid #4A743C;
    border-radius: 4px;
}
.radio-toolbar input[type="radio"]:checked + label {
    background-color: #AAD578;
    border-color: #95AD7A;
}
.radio-toolbar input[type="radio"]:focus + label {
    border: 1px solid #95AD7A;
}
.biocard {
  position: relative;
}

.biocard .content {
  position: absolute;
  width: 200px;
  bottom: 16px;
  left: 16px;
  background: rgba(255, 255, 255, 0.4);
}

.content--tag {
  padding: 8px;
  display: block;
  border-width: medium;
  border-style: solid;
  border-color: #231f20;
}

.content--tag-logo {
  padding-bottom: 8px;
}

.content--tag-facts {
  padding-top: 8px;
  padding-bottom: 8px;
  display: block;
  border-bottom-style: solid;
  border-top-style: solid;
  border-bottom-color: #231f20;
  border-bottom-width: 4px;
  border-top-width: 8px;
}

.content--tag-facts .item {
  border-bottom: solid 1px gray;
}

.content--tag-facts .item:last-child {
  border-bottom: none;
}

</style>
