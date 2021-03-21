<script>
  import { fade } from 'svelte/transition';

  let shouldFadeIn = false;
</script>

<button on:click={() => (shouldFadeIn = !shouldFadeIn)}> Fade in text</button>

{#if shouldFadeIn}
  {#each [1, 2, 3, 4, 5] as item}
    <p transition:fade={{ duration: item * 2000 }}>Now you see me</p>
  {/each}
{/if}
