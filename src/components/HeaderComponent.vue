<script setup>
</script>

<template>
  <header class="header">
    <h1 class="header-title">Hola a Todos</h1>
    <nav>
      <ul class="nav-list">
        <li><a href="#" class="link">Home</a></li>
        <li><a href="#" class="link">Blog</a></li>
        <li><a href="#" class="link">Contact Us</a></li>
      </ul>
    </nav>
  </header>
</template>

<style>
.header {
  background-color: #000022;
  color: white;
  padding: 20px;

  .header-title {
    margin: 0;
    margin-bottom: 30px;
    text-align: center;
  }

  .nav-list {
    list-style: none;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: space-around;

    .link {
      color: white;
      text-decoration: none;
    }
  }
}
</style>