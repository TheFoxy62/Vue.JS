<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import HelloWorld from './components/HelloWorld.vue';
import Komi from './components/Komi.vue';
import LoginForm from './components/LoginForm.vue';
import Navbar from './components/Navbar.vue';
</script>

<template>

  <!-- <HelloWorld /> -->
  <LoginForm />
  <Komi />
  <Navbar />
</template>

<style>
#app{

  background: linear-gradient(#1d8ecf, #8e7ddb);
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}

</style>
