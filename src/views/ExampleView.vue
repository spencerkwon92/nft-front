<template>
  <div>
    <h1>Example Page</h1>
    <div class="box-container">
      <ExampleCard v-for="n in 16" :key="n" />
    </div>
    <Button
      buttonName="Click Me!"
      fontColor="white"
      backgroundColor="black"
      size="50px"
      center="center"
    />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

import ExampleCard from "@/components/example/ExampleCard.vue";
import Button from "@/components/New-Button.vue";

export default defineComponent({
  components: {
    ExampleCard,
    Button,
  },
});
</script>

<style lang="scss" scoped>
.box-container {
  display: flex;
  flex-wrap: wrap;
}
</style>
