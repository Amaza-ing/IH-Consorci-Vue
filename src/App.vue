<script setup>
import { ref } from "vue";
import HeaderComponent from "./components/HeaderComponent.vue";
import Lists from "./components/Lists.vue";
import ParentComponent from "./components/ParentComponent.vue";
import MovieList from "./components/MovieList.vue";

const isDark = ref(false);

function toggleDark() {
  isDark.value = !isDark.value;
}
</script>

<template>
  <HeaderComponent />

  <i class="icon" @click="toggleDark">
    {{ isDark ? "🌞" : "🌚" }}
  </i>

  <!-- <section :class="{dark: isDark}">
    <Lists />
  </section> -->

  <!-- <ParentComponent /> -->

   <MovieList />
</template>

<style>
.icon {
  position: absolute;
  top: 10px;
  right: 20px;
  cursor: pointer;
  font-style: normal;
}

.dark {
  background-color: #222;
  color: white;
}
</style>
