<template>
  <div>This is an about page</div>
  <section>
    <div class="image">
      <img class="img" src="@/assets/icons/spencer.jpeg" alt="" />
    </div>
    <div class="info">
      <p class="txt-main">Hello!</p>
      <p class="txt-sub">I am Spencer!</p>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  setup() {
    return {};
  },
});
</script>

<style lang="scss" scoped>
section {
  text-align: center;

  .img {
    border-radius: 12px;
    width: 40vw;
    transition: all 0.2s linear;
  }

  .txt {
    &-main {
      font-size: 10vw;
    }
    &-sub {
      font-size: 5vw;
    }
  }
}

@media all and (min-width: 500px) {
  .img {
    float: left;
  }
}

@media all and (max-width: 499px) {
  .img {
    float: none;
  }
}
</style>
