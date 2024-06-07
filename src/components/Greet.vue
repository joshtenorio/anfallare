<script setup lang="ts">
import { ref } from "vue";
import { invoke } from "@tauri-apps/api/core";
import { Button } from "./ui/button";
import { Input } from "./ui/input";

const greetMsg = ref("");
const name = ref("");

async function greet() {
  // Learn more about Tauri commands at https://tauri.app/v1/guides/features/command
  greetMsg.value = await invoke("greet", { name: name.value });
  console.log("greeted!")
}
</script>

<template>
  <form class="row" @submit.prevent="greet">
    <div className="flex flex-row space-x-2">
      <Input id="greet-input" v-model="name" placeholder="Enter a name..." />
      <Button type="submit" variant="default">hehe</Button>
    </div>
  </form>

  <p>{{ greetMsg }}</p>
</template>
