<!-- app/javascript/app.vue -->
<template>
    <p>{{ message }}</p>
</template>

<script>
import { defineComponent, ref } from "vue";

export default defineComponent({
    setup() {
        const message = ref('Ruby on Rails + vite + Vue3!');

        return {
            message,
        };
    },
});

</script>
  
<style scoped>
p {
    font-size: 2em;
    text-align: center;
}
</style>