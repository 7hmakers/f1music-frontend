<script setup lang="ts">
const props = defineProps<{ name: string }>();
const router = useRouter();
</script>

<template>
  <div>
    <div i-carbon-pedestrian inline-block text-4xl />
    <p>
      Hi, {{ props.name }}
    </p>
    <p op50 text-sm>
      <em>Dynamic route!</em>
    </p>

    <div>
      <button
        class="btn m-3 mt-8 text-sm"
        @click="router.back()"
      >
        Back
      </button>
    </div>
  </div>
</template>
