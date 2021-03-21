<script>
  let clickCount = 0;

  async function getRandomNumber() {
    return new Promise((resolve, reject) => {
      if (clickCount > 1) {
        reject(new Error('Too many clicks!'));
      }

      setTimeout(() => {
        resolve(Math.random());
      }, 1000);
    });
  }

  let promise = getRandomNumber();

  function handleClick() {
    clickCount++;
    promise = getRandomNumber();
  }
</script>

<button on:click={handleClick}> generate random number </button>

{#await promise}
  <p>...waiting</p>
{:then number}
  <p>The number is {number}</p>
{:catch error}
  <p style="color: red">{error.message}</p>
{/await}
