<template>
  <a :href="href" class="button group">
    <span class="button__text">
      <slot></slot>
    </span>
    <span class="button__arrow">
      <span class="material-icons-round button__arrow--hover">arrow_forward</span>
      <span class="material-icons-round button__arrow--default">keyboard_arrow_right</span>
    </span>
  </a>
</template>

<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({
  name: "Button",
  props: {
    href: {
      type: String,
      default: ""
    }
  }
});
</script>

<style lang="postcss">
.button {
  @apply font-semibold rounded-full inline-flex group;
  @apply text-gray-800 bg-white no-underline bg-opacity-80 hover:bg-opacity-100 transition-colors;
  @apply px-4 py-2;
  &__arrow {
    @apply relative h-4 w-4 mr-2;
    &--default, &--hover {
      @apply transition-all duration-150 absolute w-full h-full transform left-0 top-0 leading-none;
    }
    &--default {
      @apply opacity-100 translate-x-1 text-2xl leading-none;
      @apply group-hover:opacity-0 group-hover:translate-x-0;
    }
    &--hover {
      @apply opacity-0 text-2xl leading-none;
      @apply group-hover:translate-x-1 group-hover:opacity-100;
    }
  }
  &__text {
    @apply leading-normal
  }
}
</style>