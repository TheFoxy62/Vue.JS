<script>
import {ref} from 'vue'

export default {
  data:()=>({
    activeItem: 0
  })
}
</script>

<template>  
<div>
        <img alt="Vue logo" class="w-30 h-40" src="./icons/logo food.png">
        </div>
  
      <section>
        <nav class="justify-center px-12 py-3 rounded-md w-full">
  <ol class="list-reset flex">
    <li><a href="#" class="text-blue-600 hover:text-blue-700">Accueil</a></li>
    <li><span class="text-gray-500 mx-2">/</span></li>
    <li><a href="#" class="text-blue-600 hover:text-blue-700">Menu</a></li>
    <li><span class="text-gray-500 mx-2">/</span></li>
    <li class="text-gray-500">À Propos de nous!</li>
  </ol>
</nav>
    </section>
        <div>
        <img src="./icons/hamburger.jpg" class="object- object-center pt-12 py-12" alt="Hamburger">
</div>




</template>

