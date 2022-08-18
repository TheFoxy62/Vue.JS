<template>
  <div id="app">
    <h1>Houlala</h1>
    <select v-if="categories" v-model="selectedCategorie">
      <option value="">Please Select</option>
      <option v-for="categorie in categories" v-bind:key="categorie.id" v-bind:value="categorie" >{{ categorie.name }}</option>
    </select>
    <div v-if="selectedCategorie">
      <Categorie v-bind:key="selectedCategorie.id" v-bind:categorie="selectedCategorie" @getCategories="getCategories" />
    </div>
    <div v-else>
      <Categorie v-bind:categorie="newCategorie" @getCategories="getCategories" />
    </div>
  </div>
</template>

<script>
import Categorie from './components/Categorie.vue'

export default {
  name: 'App',
  components: {
    Categorie
  },
  data () {
    return {
      selectedCategorie: null,
      newCategorie: {},
      categories: null
    }
  },
  methods: {
    getCategories: function () {
      console.log('get of categories')
      fetch('https://127.0.0.1:8000/api/categories/', { method: 'GET' })
        .then(function (response) { return response.json() })
        .then((responseJSON) => { this.categories = responseJSON['hydra:member'] })
    }
  },
  mounted () {
    this.getCategories()
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
