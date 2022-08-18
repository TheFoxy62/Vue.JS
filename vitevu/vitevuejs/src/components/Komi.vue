<script setup>
import { ref } from 'vue'

const titleClass = ref('title')
</script>

<template>
    <h1 :class="titleClass">Komi can't communicate</h1>
</template>

<style>
.title {
    text-shadow: 1px 1px 2px black;
    color: red;
}
</style>