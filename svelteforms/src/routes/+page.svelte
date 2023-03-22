<script>
  export let data;
</script>

<h1>Todos</h1>

<form method="post">
  <label>
    <input name="description" />
  </label>
  <button>submit</button>
</form>

<!-- {#each data.todos as todo}
  <ul>
    <li>{todo}</li>
  </ul>
{/each} -->
