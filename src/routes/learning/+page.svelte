<script>
  export let name = "";
  let x = 0;
  const handleIncrement = () => {
    x++;
  };
</script>

<h1>Hello {name}!</h1>
<h2>{x}</h2>
{#if x < 5}
  <p>{x} is less than 5</p>
{:else if (x = 5)}
  <p>{x} is equal 5</p>
{:else if x > 5}
  <p>{x} is greater than 5</p>
{/if}
<button on:click={handleIncrement}>Increment</button>

<style>
  h1 {
    color: red;
  }
</style>
