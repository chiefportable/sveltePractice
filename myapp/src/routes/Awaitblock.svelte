<script>
  let m = { x: 0, y: 0 };
  function handleMousemove(event) {
    m.x = event.clientX;
    m.y = event.clientY;
  }

  function handleClick(event) {
    event.preventDefault();
    alert("no more alert");
  }
</script>

<div on:mousemove={handleMousemove}>
  The mouse position is {m.x} x {m.y}
</div>

<button on:click={handleClick}>click me!!</button>

<form action="" method="post">
  <input type="text" placeholder="Enter name" />
  <input type="submit" value="submit" on:click={handleClick} />
</form>
