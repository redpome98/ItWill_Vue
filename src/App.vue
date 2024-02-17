<script setup>
import { ref, reactive } from "vue";
const title = ref("Item List");
const items = ref(["RickenBacker", "StringRay", "Fender", "Squier", "G&L"]);
const justice = "./justice.png";
const typeText = ref("");

function BtnEvent() {
  alert("You clicked Button");
}

const BtnConsole = () => {
  console.log(items.value); // value
};
</script>

<template>
  <h1>Gimme my money in stacks</h1>
  <hr />
  <img :src="justice" width="480px" height="300px" />
  <button @click="BtnEvent">Click</button>
  <button @click="BtnConsole">Console</button><br /><br />
  양방향 테스트 : <input v-model="typeText" type="text" />
  <h3>{{ title }}</h3>
  <ul>
    <li v-for="goods in items">{{ goods }}</li>
  </ul>
  <h3>Copyright by Song 2024 vue</h3>
</template>

<style scoped>
h1 {
  color: crimson;
}
</style>
