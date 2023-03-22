<script>
  import Custombutton from "./Custombutton.svelte";
  function handleClick() {
    alert("buttom clicked");
  }
</script>

<Custombutton on:click={handleClick} />
