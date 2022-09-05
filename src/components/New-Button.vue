<template>
  <div :style="cssVars">
    <button @click="onClick" :style="cssVars">
      {{ buttonName }}
    </button>
  </div>
  <div v-if="isModule">
    <Module header="This is header" @close="onClick">
      <h3>Here is contents</h3>
    </Module>
  </div>
</template>

<script>
import { defineComponent } from "vue";
import Module from "./New-Module.vue";

export default defineComponent({
  data() {
    return {
      isModule: false,
    };
  },
  methods: {
    onClick() {
      this.isModule = !this.isModule;
    },
  },
  props: ["buttonName", "backgroundColor", "size", "fontColor", "center"],
  computed: {
    cssVars() {
      return {
        "--backgroundColor": this.backgroundColor,
        "--fontColor": this.fontColor,
        "--fontSize": this.size,
        "--center": this.center,
      };
    },
  },
  components: { Module },
});
</script>

<style lang="scss" scoped>
div {
  text-align: var(--center);
}
button {
  background-color: var(--backgroundColor);
  color: var(--fontColor);
  font-size: var(--fontSize);
}
</style>
