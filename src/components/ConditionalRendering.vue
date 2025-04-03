<script setup>
import { ref } from 'vue';

const user = ref({
  username: "Adrián",
  isLoggedIn: true,
});
</script>

<template>
  <section v-if="user.isLoggedIn">
    <h2>Título de la sección</h2>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam, sint,
      maxime ea voluptatum accusantium corporis eius consequatur, facilis
      perspiciatis cum nobis libero debitis. Laudantium quia cupiditate qui
      nostrum ipsum perferendis!
    </p>
  </section>
  <section v-else>
    <h2>Inicia sesión para ver el contenido</h2>
  </section>
</template>

<style></style>