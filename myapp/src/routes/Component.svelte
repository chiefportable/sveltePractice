<script>
  let name = "";
  let a = "";
  let b = 5;
  let yes = false;

  $: console.log(yes);
</script>

<input type="text" bind:value={name} />
<input type="number" bind:value={b} min="0" max="10" />
<input type="range" bind:value={b} min="0" max="10" />
<input type="checkbox" bind:checked={yes} />
{#if yes == true}
  <p>checkbox checked</p>
{:else}
  <p />
{/if}

<p>Hello {name}</p>

<button on:message>click</button>
