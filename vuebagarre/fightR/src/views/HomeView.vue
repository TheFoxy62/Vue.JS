<script setup>
import { ref } from 'vue';
import { useCounterStore } from '../stores/counter';

// methode store
const storeCounter = useCounterStore()

// methode a la main
const count = ref(0)

const increment= () => {
  count.value++
}

const decrease = () => {
  count.value--
}
</script>

<template>

<section>
<div>
  <img src="../components/images/250px-Pikachu-DEPS.png">
  <div>
    <br>
    <button class="positif" @click="storeCounter.increment">+</button>
    <button class="négative" @click="storeCounter.decrease">-</button>
    <p>
      StoreCounter: {{storeCounter.counter}}
    </p>
    </div>
  </div>
</section>
<br>
<section>
<div>
  <img src="../components/images/carapuce.png">
  <div>
    <br>
    <button class="positif" @click="storeCounter.increment">+</button>
    <button class="négative" @click="storeCounter.decrease">-</button>
    <p>
      StoreCounter: {{storeCounter.counter}}
    </p>
    </div>
  </div>
</section>

<button class="Start" onclick="move()">Acheter</button> 


  <!-- <button @click="increment">+</button>
  <button @click="decrease">-</button> -->
</template>

<style>
img{
  text-align: center;
}
</style>
