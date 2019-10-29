<template>
  <div id="biofacts" class="ui container">
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
        <div class="ui four stackable cards">
          <div class="card" v-for="(product, index) in computedProducts" :key="index">
            <img :src="product.img_url" alt="" class="ui image">
            <div class="content">
              <h4 class="ui header">{{product.name}}</h4>
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
  name: 'BioFacts',
  el: '#biofacts',
  data() {
    return {
      categories: [ ],
      years: [ ],
      products: [
        {name:'Vidrio', year:'4000', category:'vidrio', img_url:'http://biofacts.org/wp-content/uploads/2018/09/fact_vidrio-500x500.jpg'},
        {name:'Botella Nueva', year:'4000', category:'vidrio', img_url:'http://biofacts.org/wp-content/uploads/2018/09/fact_vidrio-500x500.jpg'},
        {name:'Lata de Aluminio', year:'50', category:'aluminio', img_url:'http://biofacts.org/wp-content/uploads/2018/09/fact_lata_mobile-500x500.jpg'},
        {name:'Botella de PET', year:'150', category:'pet', img_url:'http://biofacts.org/wp-content/uploads/2018/09/fact_botella-1-500x500.jpg'},
        {name:'Polipropileno', year:'1000', category:'polipropileno', img_url:'http://biofacts.org/wp-content/uploads/2018/09/fact_polipropileno-1-500x500.jpg'},
        {name:'Bolsa de Plastico', year:'400', category:'plastico', img_url:'http://biofacts.org/wp-content/uploads/2018/09/fact_bolsa-500x500.jpg'},
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
#biofacts {
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
</style>
