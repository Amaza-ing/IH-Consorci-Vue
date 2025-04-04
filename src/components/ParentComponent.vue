<script setup>
import ChildComponent from "./ChildComponent.vue";

const message = "Otro mensaje desde el padre";

function displayAlert(msg) {
  alert(msg);
}
</script>

<template>
  <section class="parent">
    <h2>Este es el componente Padre</h2>

    <div class="child">
      <ChildComponent
        title="Texto desde el padre"
        @send-message="displayAlert"
      />
    </div>
    <div class="child">
      <ChildComponent :title="message" @send-message="displayAlert" >
        <p>HTML inyectado desde el padre</p>
      </ChildComponent>
    </div>
  </section>
</template>

<style>
.parent {
  padding: 20px;
  margin: 10px;
  border: 2px solid black;
}

.child {
  padding: 10px;
  margin: 10px;
  border: 2px dashed darkblue;
}
</style>
