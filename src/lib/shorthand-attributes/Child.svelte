<script lang="ts">
  export let message: string;

  let blue = true;
</script>

<button class:blue>{message}</button>

<style>
  .blue {
    color: blue;
  }
</style>
