<script>
  let questions = [
    {
      id: 1,
      text: `where did you go to school?`,
    },
    {
      id: 2,
      text: `what is your mother's name?`,
    },
    {
      id: 3,
      text: `What is your pet's name?`,
    },
  ];

  let selected;
  let answer = "";

  function handleSubmit() {
    alert(
      `answered question ${selected.id} (${selected.text}) with "${answer}"`
    );
  }
</script>

<h2>Insecurity questions</h2>

<form>
  <select value={selected} on:change={() => (answer = "")}>
    {#each questions as question}
      <option value={question}>
        {question.text}
      </option>
    {/each}
  </select>

  <input bind:value={answer} />

  <button disabled={!answer}>submit</button>
</form>

<p>
  selected question {selected ? selected.id : "[waiting.....]"}
</p>

<style>
  input {
    display: block;
    width: 500px;
    max-width: 100%;
  }
</style>
