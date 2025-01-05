<script>
 import { onMount } from 'svelte';
 export let lang = 'en';
 let content = '';

 onMount(async () => {
  const response = await fetch('/terms_' + lang + '.html');
  content = await response.text();
 });
</script>

<style>
 .terms :global(.title) {
  font-size: 20px;
  font-weight: bold;
  padding-bottom: 10px;
 }
</style>

<div class="terms">
 {@html content}
</div>
