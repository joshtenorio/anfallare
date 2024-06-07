<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import Greet from "./components/Greet.vue";
import { ModeToggle } from "./components/ui/mode-toggle";
</script>

<template>
  <div class="container">
    <h1>Welcome to Tauri!</h1>
    <ModeToggle />
    <p>Click on the Tauri, Vite, and Vue logos to learn more.</p>

    <Greet />
  </div>
</template>
