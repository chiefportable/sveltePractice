<script>
  let count = 0;
  function increment() {
    count += 1;
  }

  function decrease() {
    if (count === 0) {
      count = 0;
    } else {
      count -= 1;
    }
  }

  $: doubled = count * 2;

  $: if (count >= 10) {
    alert("number is dangerously up");
    count = 0;
  }
</script>

<p>{count}</p>

<button on:click={increment}>+</button>
<button on:click={decrease}>-</button>

<p>{count} doubled is {doubled}</p>
