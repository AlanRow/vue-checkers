<template>
  <checkers-map :map="map" />
</template>

<script setup lang="ts">
import CheckersMap from "./components/CheckersMap.vue";
import { CheckersMapData } from "./types/CheckersMap";

const map: CheckersMapData = [
  [null, "white", null, "white", null, "white", null, "white"],
  ["white", null, "white", null, "white", null, "white", null],
  [null, "white", null, "white", null, "white", null, "white"],
  [null, null, null, null, null, null, null, null],
  [null, null, null, null, null, null, null, null],
  ["black", null, "black", null, "black", null, "black", null],
  [null, "black", null, "black", null, "black", null, "black"],
  ["black", null, "black", null, "black", null, "black", null],
];
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
