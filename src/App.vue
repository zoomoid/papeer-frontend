<template>
  <papeer-header class="header"></papeer-header>
  <main></main>
  <papeer-footer class="footer"></papeer-footer>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import PapeerFooter from './components/Footer.vue'
import PapeerHeader from './components/Header.vue'

export default defineComponent({
  name: 'App',
  components: {
    PapeerHeader,
    PapeerFooter
  }
})
</script>

<style lang="postcss">
#app {
  @apply font-mono;
  @apply min-h-screen;
  @apply flex flex-col;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
main {
  @apply flex-grow;
}
</style>