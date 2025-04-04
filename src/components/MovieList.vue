<script setup>
import { ref } from "vue";
import MovieCard from "./MovieCard.vue";

const movies = ref([
  {
    id: 1,
    title: "El Señor de los Anillos",
    img: "https://m.media-amazon.com/images/M/MV5BNDM0ZTRjNDAtMWFiOS00MjZiLThhZjYtNGQ0ODQ5MGE3Y2Y0XkEyXkFqcGc@._V1_FMjpg_UX1000_.jpg",
    duration: 300,
    hasAnyOscars: true,
  },
  {
    id: 2,
    title: "Star Wars",
    img: "https://i.blogs.es/1da08b/1366_2000-9-/1366_2000.jpeg",
    duration: 120,
    hasAnyOscars: true,
  },
  {
    id: 3,
    title: "Dune",
    img: "https://es.web.img3.acsta.net/c_310_420/pictures/24/02/20/17/42/2385575.jpg",
    duration: 200,
    hasAnyOscars: false,
  },
]);

function deleteMovie(id) {
  const movieIndex = movies.value.findIndex((movie) => movie.id === id);

  movies.value.splice(movieIndex, 1);
}
</script>

<template>
  <h2>Movies:</h2>

  <ul class="movie-list">
    <li v-for="movie in movies" :key="movie.id">
      <MovieCard :movie="movie" @delete-movie="deleteMovie" />
    </li>
  </ul>
</template>

<style>
.movie-list {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
}
</style>
