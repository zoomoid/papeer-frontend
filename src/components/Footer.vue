<template>
  <footer>
    <div class="wrapper">
      <div>
        <h2>Papeer</h2>
        <p>
          Publish and pre-release papers from Gitlab CI using micro-service
          wizardry, MinIO and NodeJS + vitejs.
        </p>
        <p>Made by <a href="https://github.com/zoomoid">zoomoid</a> in 2021.</p>
        <papeer-button href="https://github.com/zoomoid/papeer"
          >See how it's done</papeer-button
        >
      </div>
    </div>
  </footer>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import PapeerButton from "./Button.vue";
export default defineComponent({
  name: "Footer",
  components: {
    PapeerButton,
  },
});
</script>

<style lang="postcss" scoped>
footer {
  @apply bg-gray-900 text-white text-opacity-80 sm:px-12 px-4 py-4 pb-8;
  .wrapper {
    @apply grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 grid-flow-row;
  }
  h2 {
    @apply text-lg font-extrabold leading-loose;
  }
  p {
    @apply leading-snug mb-4;
    a {
      @apply text-white text-opacity-100;
    }
  }
}
</style>