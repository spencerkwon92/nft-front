<template>
  <the-header />
  <router-view />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import TheHeader from "./components/TheHeader.vue";

export default defineComponent({
  components: {
    TheHeader,
  },
});
</script>

<style scoped></style>
