<script setup>
import { ref } from 'vue';
import HeaderComponent from './components/HeaderComponent.vue';

let text = "Soy un texto que viene de una variable";
const counter = ref(0);

setInterval(() => {
  counter.value = counter.value + 1;
}, 1000);
</script>

<template>
  <HeaderComponent />

  <h2>{{ counter }}</h2>

  <h2 class="title">Bienvenidos a mi Web</h2>

  <p>
    Lorem, ipsum dolor sit amet consectetur adipisicing elit. Placeat dolorum
    tenetur magnam illum laborum nemo accusamus debitis? Delectus ipsam
    molestias voluptate repellat ab, fuga animi, fugit, maxime labore aliquid
    quaerat!
  </p>
  <p>{{ text }}</p>
</template>

<style>
.title {
  background-color: yellow;
}
</style>
