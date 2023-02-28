<script setup lang="ts" generic="T extends any, O extends any">
defineOptions({
  name: "IndexPage",
});

const name = $ref("");

const router = useRouter();
const go = () => {
  if (name) { router.push(`/hi/${encodeURIComponent(name)}`); }
};
</script>

<template>
  <div>
    <div i-carbon-campsite inline-block text-4xl />
    <p>
      <a href="https://github.com/antfu/vitesse-lite" rel="noopener noreferrer" target="_blank">
        Vitesse Lite
      </a>
    </p>
    <p>
      <em op75 text-sm>Opinionated Vite Starter Template</em>
    </p>

    <div py-4 />

    <TheInput
      v-model="name"
      autocomplete="false"
      placeholder="What's your name?"
      @keydown.enter="go"
    />

    <div>
      <button
        class="btn m-3 text-sm"
        :disabled="!name"
        @click="go"
      >
        Go
      </button>
    </div>
  </div>
</template>
