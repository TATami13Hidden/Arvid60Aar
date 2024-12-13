<script setup>
import Button from 'primevue/button';

const maxNumber = 8;
let rand = Math.floor(Math.random() * maxNumber + 1);
let rand1 = 0;
while (rand1 === rand || rand1 === 0) {
  rand1 = Math.floor(Math.random() * maxNumber + 1);
}

</script>

<template>
  <header>
  </header>
  <main>
    <div class="flex-row">
      <div><img :src="`/src/images/image${rand}.jpg`" alt="random image of dad"></div>
      <div class="layout">
        <Button><a href="https://fb.me/1Xtnc0HVC37UyOv">Facebook</a></Button>
      </div>
      <div><img :src="`/src/images/image${rand1}.jpg`" alt="random image of dad"></div>
    </div>
  </main>
</template>

<style scoped>
.layout {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  gap: 1rem;
}
header {
  width: 100vw;
  padding: 1rem;
}
nav {
  display: flex;
  gap: 1rem;
  justify-content: space-between;
}
a {
  color: white;
  padding: 10px;
  border-radius: 10px;
}
main {
  display: flex;
  justify-content: center;
  align-content: center;
}
.flex-row {
  display: flex;
  flex-direction: row;
  gap: 1rem;
  width: 100%;
}
.flex-row > div {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}
.flex-row img {
  width: 100%;
  height: auto;
}

</style>
