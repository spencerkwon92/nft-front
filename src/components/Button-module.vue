<template>
  <div class="backdrop" @click="closeModule">
    <div class="modal">
      <h1>{{ header }}</h1>
      <slot></slot>
    </div>
  </div>
</template>

<script>
import { defineComponent } from "vue";
export default defineComponent({
  methods: {
    closeModule() {
      this.$emit("close");
    },
  },
  props: ["header"],
});
</script>

<style lang="scss" scoped>
.modal {
  width: 400px;
  padding: 20px;
  margin: 100px auto;
  background-color: white;
  border-radius: 10px;
}
.backdrop {
  top: 0;
  position: fixed;
  background-color: rgba(0, 0, 0, 0.5);
  width: 100%;
  height: 100%;
}
</style>
