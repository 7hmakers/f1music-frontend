<script setup lang="ts">
const { modelValue } = defineModel<{
  modelValue: string
}>();
</script>

<template>
  <input
    v-model="modelValue"
    id="input"
    v-bind="$attrs"
    bg="transparent"
    border="~ rounded gray-200 dark:gray-700"
    outline="none active:none"
    p="x-4 y-2"
    text="center"
    type="text"
    w="250px"
  >
</template>
