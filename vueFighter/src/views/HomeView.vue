<script setup>
import TheWelcome from '@/components/TheWelcome.vue'

import {ref} from 'vue'

const count = ref(0)
const count2 = ref(0)

</script>

<template>
  <main>
    <TheWelcome />
  </main>

  <button type="button" @click="count++">count is: {{ count }}</button>-
  <button type="button" @click="count2++">count2 is: {{ count2 }}</button>

</template>
