<template>
  <div>
    <h1>Example Page</h1>
    <div class="box-container">
      <ExampleCard v-for="n in 16" :key="n" />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import ExampleCard from "@/components/example/ExampleCard.vue";

export default defineComponent({
  components: {
    ExampleCard,
  },
});
</script>

<style lang="scss" scoped>
.box-container {
  display: flex;
  flex-wrap: wrap;
}
</style>
