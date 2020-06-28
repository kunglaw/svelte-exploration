<script>
  export let name; // ini artinya props yang dijadikan state
  export let changeName;

  let color = "green";

  function helloPerson() {
    alert("Hello " + name);
  }
</script>

<main>
  <p>child component :</p>
  <h1 style="color:{color};font-style:italic">Dio Says : {name}</h1>
  <input type="text" name="name" bind:value={name} on:keyup={changeName} />
  <select bind:value={color}>
    <option>red</option>
    <option>green</option>
    <option>blue</option>
  </select>
  <button on:click={helloPerson}>Greet this person</button>
</main>
