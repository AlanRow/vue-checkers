<template>
  <table class="checkers-desk">
    <tr
      v-for="(row, rowIndex) in props.map"
      :key="rowIndex"
      class="checkers-row"
    >
      <th v-for="(cell, index) in row" :key="index" class="checkers-cell"></th>
    </tr>
  </table>
</template>

<script setup lang="ts">
import { CheckersMapData } from "@/types/CheckersMap";

const props = defineProps<{
  map: CheckersMapData;
}>();
</script>

<style scoped lang="scss">
.checkers-desk {
  border: 2px solid black;

  .checkers-row {
    .checkers-cell {
      width: 50px;
      height: 50px;
    }

    &:nth-child(even) {
      .checkers-cell:nth-child(even) {
        background-color: white;
      }
      .checkers-cell:nth-child(odd) {
        background-color: black;
      }
    }
    &:nth-child(odd) {
      .checkers-cell:nth-child(even) {
        background-color: black;
      }
      .checkers-cell:nth-child(odd) {
        background-color: white;
      }
    }
  }
}
</style>
