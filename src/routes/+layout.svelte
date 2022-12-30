<script>
  import "../app.css";
  import { Footer, FooterCopyright, FooterLinkGroup, FooterBrand, FooterLink } from 'flowbite-svelte'
  import Sidebar from "$lib/Sidebar.svelte";
  // On page load or when changing themes, best to add inline in `head` to avoid FOUC
  if (localStorage.theme === 'dark' || (!('theme' in localStorage) && window.matchMedia('(prefers-color-scheme: dark)').matches)) {
    document.documentElement.classList.add('dark')
  } else {
    document.documentElement.classList.remove('dark')
  }

  // Whenever the user explicitly chooses light mode
  localStorage.theme = 'light'

  // Whenever the user explicitly chooses dark mode
  localStorage.theme = 'dark'

  // Whenever the user explicitly chooses to respect the OS preference
  localStorage.removeItem('theme')
</script>

<div id = "boxes">
    <div id = "leftbox">
        <Sidebar></Sidebar>
    </div>

    <div id = "rightbox">
        <slot></slot>
    </div>
</div>

<style>
    #leftbox {
        float:left;
        width:20%;
        height: 500px;
    }
    #rightbox{
        float:right;
        width:80%;
        height: 500px;
    }
</style>
