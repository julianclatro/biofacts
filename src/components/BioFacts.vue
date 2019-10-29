<template>
  <div id="card">
    <div class="ui container" style="margin-top: 20px;">
      <h1>Calculadora de Materiales</h1>
      <div class="ui segment">
        <h3 class="ui header">
        Elije un material a continuación:
        </h3>
        <!-- 50: <input type="checkbox" v-model="years" value="50"/>
        150: <input type="checkbox" v-model="years" value="150"/>
        400: <input type="checkbox" v-model="years" value="400"/>
        1000: <input type="checkbox" v-model="years" value="1000"/>
        4000: <input type="checkbox" v-model="years" value="4000"/> -->
        <div class="radio-toolbar">
          <input type="radio" v-model="categories" id="radioTodos" value="" checked />
          <label for="radioTodos">Todos</label>
          <input type="radio" v-model="categories" id="radioAluminio" value="aluminio"/>
          <label for="radioAluminio">Aluminio</label>
          <input type="radio" v-model="categories" id="radioPlastico" value="plastico"/>
          <label for="radioPlastico">Plastico</label>
          <input type="radio" v-model="categories" id="radioPet" value="pet"/>
          <label for="radioPet">Pet</label>
          <input type="radio" v-model="categories" id="radioVidrio" value="vidrio"/>
          <label for="radioVidrio">Vidrio</label>
          <input type="radio" v-model="categories" id="radioPolipropileno" value="polipropileno"/>
          <label for="radioPolipropileno">Polipropileno</label>
          <input type="radio" v-model="categories" id="radioCarton" value="carton"/>
          <label for="radioCarton">Carton</label>
        </div>
      </div>
      <div class="ui three cards">
        <div class="card" v-for="(product, index) in computedProducts" :key="index">
          <img :src="product.img_url" alt="" class="ui image">
          <div class="content">
            <h4 class="ui header">{{product.name}}</h4>
          </div>
        </div>
      </div>
      <h1>Etiquetas</h1>
      <div v-for="(product, index) in computedProducts" :key="index">
      <div>{{product.name}}</div>
      <div>{{product.year}}</div>
      <div>{{product.category}}</div>
      </div>
    </div>
  </div>
</template>

<script>
// import Paginate from 'vuejs-paginate'
// Vue.component('paginate', Paginate)
export default {
  name: 'BioFacts',
  el: '#card',
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
        {name:'Bolsa de Plastico', year:'400', category:'plastico', img_url:'http://biofacts.org/wp-content/uploads/2018/09/fact_bolsa-500x500.jpg'},
        {name:'Vaso de Carton', year:'50', category:'carton', img_url:'https://images.unsplash.com/photo-1564674705242-8e1cfca3674e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=934&q=80'}
      ],
      sortBy: 'name'
    }
  },
  computed: {
    computedProducts: function () {
      return this.products.filter((item) => {
        console.log(item.category)
        console.log(this.years)
        console.log(this.categories.includes(item.category))
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
#card {
  padding-top: 40px;
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
  margin: 0 10px;
}
a {
  color: #42b983;
}
.radio-toolbar input[type="radio"] {
  opacity: 0;
  position: fixed;
  width: 0;
}
.radio-toolbar label {
    display: inline-block;
    background-color: #ddd;
    padding: 12px 12px 8px 12px;
    margin: 4px;
    font-family: 'Poppins', sans-serif;
    font-size: 16px;
    font-weight: 600;
    border: 2px solid #444;
    border-radius: 4px;
}
.radio-toolbar input[type="radio"]:checked + label {
    background-color:#bfb;
    border-color: #4c4;
}
.radio-toolbar input[type="radio"]:focus + label {
    border: 2px dashed #444;
}
</style>
