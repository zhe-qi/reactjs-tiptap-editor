<script setup lang="ts">
import { contributors } from '../../../scripts/contributors';
</script>

<template>
  <div class="vp-doc">
    <h2 class="op50 font-normal pt-5 pb-2">
      Contributors
    </h2>
  </div>
  <div class="text-lg max-w-200 text-center leading-7 p-10">
    <div class="flex flex-wrap gap-1 justify-center">
      <a v-for="{ name, avatar } of contributors" :key="name" :href="`https://github.com/${name}`" class="m-0" rel="noopener noreferrer" :aria-label="`${name} on GitHub`">
        <img loading="lazy" :src="avatar" width="40" height="40" class="rounded-full min-w-10 min-h-10 h-10 w-10" :alt="`${name}'s avatar`">
      </a>
    </div>
    <br>
  </div>
</template>
