<template>
  <button :class="$style.button" :data-color="props.color">
    <slot></slot>
  </button>
</template>

<script setup lang="ts">
import { UiButtonProps } from "../types";

const props = withDefaults(defineProps<UiButtonProps>(), {});
</script>

<style module>
.button {
  display: inline-flex;
  padding: 16px 32px;
  cursor: pointer;
  border: 0;
  border-radius: 16px;
}

.button[data-color="primary"] {
  background-color: var(--color-primary);
}

.button[data-color="gray"] {
  background-color: var(--color-gray);
}
</style>
../types
