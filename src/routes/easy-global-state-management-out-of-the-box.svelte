<script>
  import { isDev } from '../stores.js';
</script>

{#if $isDev}
  <p>This paragraph is only shown in dev mode</p>
{:else}
  <p>This paragraph is only shown in production mode</p>
{/if}
