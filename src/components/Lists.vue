<script setup>
const names = ["Ana", "Luis", "Carlos"];

const products = [
  {
    id: 1,
    name: "Ordenador",
    price: 1000,
    isAvailable: true,
  },
  {
    id: 2,
    name: "Teclado",
    price: 50,
    isAvailable: true,
  },
  {
    id: 3,
    name: "Ratón",
    price: 20,
    isAvailable: false,
  },
];
</script>

<template>
  <ul>
    <li v-for="(name, index) in names" :key="index">
      {{ name }}
    </li>
  </ul>

  <ul class="product-list">
    <li class="product-item" v-for="product in products" :key="product.id">
      <!-- <div v-if="product.isAvailable"> -->
        <div :class="{notavailable: !product.isAvailable}">
          <h2>{{ product.name }}</h2>
          <h3 class="price">{{ product.price }} €</h3>
        </div>
      <!-- </div> -->
    </li>
  </ul>
</template>

<style>
.product-list {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
  flex-wrap: wrap;
  gap: 20px;

  .notavailable {
    .price {
      text-decoration: line-through;
    } 
  }

  .product-item {
    background-color: #ccc;
    padding: 0 20px;
    width: 150px;
  }
  .product-item:hover {
    background-color: lightcoral;
    cursor: pointer;
  }
}
</style>
