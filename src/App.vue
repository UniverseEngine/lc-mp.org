<script setup>
import { RouterLink, RouterView } from 'vue-router'
import DiscordIcon from "@/components/icons/DiscordIcon.vue";
</script>

<template>
  <div class="sm:w-1/2 m-auto p-5 text-sm">
    <img class="flex w-1/3 m-auto p-2" src="@/assets/lcmp_1.png" width="600"/>
    <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/download">Download</RouterLink>
      <a href="https://forum.lc-mp.org">Forum</a>
      <a href="https://wiki.lc-mp.org">Wiki</a>
      <RouterLink to="/about">About</RouterLink>
    </nav>

    <RouterView class="p-5 mt-1 rounded-xl bg-gray-200" />
  </div>

  <div class="flex justify-center">
    <a class="discord" href="https://discord.gg/CcYjFQd2uF">
      <DiscordIcon class="inline"/>
      Discord
    </a>
  </div>
</template>

<style scoped>
nav {
  @apply flex flex-row flex-wrap items-center justify-between border bg-yellow-500 rounded-xl p-1;
}

router-link {
  @apply p-2 pl-5 pr-5 mt-3;
}

.router-link-active {
  @apply font-bold;
}
</style>
