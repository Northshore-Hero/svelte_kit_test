<script>
  import Greet from "$lib/Greet.svelte";
  import Download from "$lib/Download.svelte";
  import {  Heading, P, Button } from 'flowbite-svelte'
</script>

<div class="pt-4">
  <Heading tag="h1" class="mb-4" customSize="text-4xl font-extrabold  md:text-5xl lg:text-2xl">Tauri and Svelt Development</Heading>
</div>

<div class="pt-4 row">
  <a href="https://vitejs.dev" target="_blank">
    <img src="/vite.svg" class="logo vite" alt="Vite Logo" />
  </a>
  <a href="https://tauri.app" target="_blank">
    <img src="/tauri.svg" class="logo tauri" alt="Tauri Logo" />
  </a>
  <a href="https://kit.svelte.dev" target="_blank">
    <img src="/svelte.svg" class="logo svelte" alt="Svelte Logo" />
  </a>
</div>

<div class ="pt-4 row">
  <p>Click on the Tauri, Vite, and Svelte logos to learn more.</p>
</div>

<div class="pt-4 row">
  <Greet />
</div>

<div class="pt-4 row">
  <Download />
</div>

<style>
  .logo.vite:hover {
    filter: drop-shadow(0 0 2em #747bff);
  }

  .logo.svelte:hover {
    filter: drop-shadow(0 0 2em #ff3e00);
  }
</style>