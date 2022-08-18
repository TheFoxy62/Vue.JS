<template>
    <div class="categorie">
      <h1 v-if="categorie.name">{{ categorie.name }}</h1>
      <h1 v-else>Créer une catégorie</h1>
      <input type="text" v-model="categorie.name" placeholder="définissez le nom de la catégorie…">
      <button v-on:click="saveCategorie">💾</button>
      <button v-on:click="deleteCategorie">🗑</button>
    </div>
</template>

<script>
export default {
  name: 'Categorie',
  props: {
    categorie: Object
  },
  methods: {
    saveCategorie () {
      if ('@id' in this.categorie) {
        fetch('https://127.0.0.1:8000/api/categories' + this.categorie['@id'], {
          method: 'PUT',
          headers: {
            'Content-Type': 'application/json'
          },
          body: JSON.stringify({ name: this.categorie.name })
        }).then(r => { this.$emit('getCategories') })
      } else {
        fetch('https://127.0.0.1:8000/api/categories/', {
          method: 'POST',
          headers: {
            'Content-Type': 'application/json'
          },
          body: JSON.stringify({ name: this.categorie.name })
        }).then(r => { this.$emit('getCategories') })
      }
    },
    deleteCategorie () {
      fetch('https://127.0.0.1:8000/api/categories' + this.categorie['@id'], { method: 'DELETE' })
        .then(r => { this.$emit('getCategories') })
    }
  }
}
</script>

<style scoped>
.categorie {
  margin: 10px; padding: 5px 10px 15px 5px;
  border: solid 1px #000;
  border-radius: 15px;
  background-color: #444;
  color: #ccc;
}
</style>
