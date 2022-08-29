<template>
  <em class="square"></em>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({});
</script>

<style lang="scss" scoped>
.square {
  width: 400px;
  height: 400px;
  background: linear-gradient(blue, red);
  margin: 20px;

  &:hover {
    background: linear-gradient(orange, brown);
  }
}
</style>
