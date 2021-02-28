<template>
  <header>
    <div class="wrapper">
      <h1>Papeer</h1>
    </div>
  </header>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Footer from "./Footer.vue";
export default defineComponent({
  components: { Footer },
  name: "Header",
});
</script>

<style lang="postcss" scoped>
header {
  @apply sm:px-12 px-4 py-8 bg-gray-900 text-white;
  h1 {
    @apply font-bold text-2xl sm:text-4xl;
  }
}
</style>