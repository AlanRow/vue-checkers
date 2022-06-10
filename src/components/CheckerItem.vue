<template>
  <div :class="['checker', `checker_type_${props.type}`]"></div>
</template>

<script lang="ts">
export default {
  name: "CheckerItem",
};
</script>

<script setup lang="ts">
const props = defineProps<{
  type: "black" | "white";
}>();
</script>

<style scoped lang="scss">
.checker {
  width: 40px;
  height: 40px;
  margin: auto;
  border-radius: 50%;
  border-width: 2px;
  border-style: solid;

  &_type {
    &_black {
      background-color: black;
      border-color: white;
    }
    &_white {
      background-color: white;
      border-color: black;
    }
  }
}
</style>
