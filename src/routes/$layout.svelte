<main>
  <h1>Hello WeAreDevelopers Live Days!</h1>
  <img src="/svelte-vertical.svg" alt="Svelte Logo" />
  <slot />
</main>

<style>
  :root {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
      Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  }

  :global(body) {
    margin: 0;
    position: relative;
  }

  :global(html),
  :global(body),
  :global(#svelte) {
    width: 100%;
    height: 100%;
  }

  main {
    position: relative;
    padding-top: 15px;
    padding-left: 15px;
    height: calc(100% - 15px);
  }

  h1 {
    color: #ff3e00;
    font-size: 4rem;
    font-weight: 100;
    line-height: 1.1;
    margin-top: 0;
  }

  img {
    opacity: 0.1;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: -1;
    width: 500px;
  }
</style>
