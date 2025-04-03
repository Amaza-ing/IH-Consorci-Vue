<script setup>
import { ref } from "vue";
import HeaderComponent from "./components/HeaderComponent.vue";

let text = "Soy un texto que viene de una variable";
const counter = ref(0);
const username = ref("");
const clickX = ref(0);
const clickY = ref(0);

const imgInfo = {
  url: "https://upload.wikimedia.org/wikipedia/commons/thumb/e/e4/Cuesta_del_obispo_01.jpg/640px-Cuesta_del_obispo_01.jpg",
  alt: "Imagen de un paisaje",
  width: 300,
};

setInterval(() => {
  counter.value = counter.value + 1;
}, 1000);

function showAlert() {
  alert("Hola a todos!");
}

function changeUsername() {
  username.value = "Adrián";
}

function handleClick(e) {
  console.log(e);
  clickX.value = e.screenX;
  clickY.value = e.screenY;
}
</script>

<template>
  <HeaderComponent />

  <img :src="imgInfo.url" :alt="imgInfo.alt" :width="imgInfo.width" />

  <h2>{{ username }}</h2>
  <input type="text" placeholder="Escribe tu Nombre" v-model="username">
  <br>
  <button @click="changeUsername">Change Username</button>

  <h2>{{ counter }}</h2>

  <h2 class="title" @click="showAlert">Bienvenidos a mi Web</h2>

  <p @click="handleClick">
    Lorem, ipsum dolor sit amet consectetur adipisicing elit. Placeat dolorum
    tenetur magnam illum laborum nemo accusamus debitis? Delectus ipsam
    molestias voluptate repellat ab, fuga animi, fugit, maxime labore aliquid
    quaerat!
  </p>
  <h3>X: {{ clickX }} - Y: {{ clickY }}</h3>
  <p>{{ text }}</p>
</template>

<style>
.title {
  background-color: yellow;
}
</style>
