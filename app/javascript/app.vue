<template>
    <p>{{ message }}</p>
</template>

<script setup>
import { ref } from "vue";

const message = ref('Ruby on Rails + vite + Vue3!');

</script>
  
<style>
p {
    font-size: 2em;
    text-align: center;
}
</style>