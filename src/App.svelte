<script>
  let num1 = null;
  let num2 = null;
  let resultado = 0;

  function suma() {
    resultado = num1 + num2;
  }

  function resta() {
    resultado = num1 - num2;
  }

  function multiplica() {
    resultado = num1 * num2;
  }

  function divide() {
    if (num2 !== 0) {
      resultado = num1 / num2;
    } else {
      resultado = 999999999999999;
    }
  }
</script>

<div>
  <h1>Calculadora</h1>

  <input type="number" bind:value={num1} placeholder="Numero 1"/>
  <input type="number" bind:value={num2} placeholder="Numero 2"/>

  <br><br>

  <div>
    <button on:click={suma}>Sumar</button>
    <button on:click={resta}>Restar</button>
    <button on:click={multiplica}>Multiplicacionr</button>
    <button on:click={divide}>Division</button>
  </div>

  <p>Resultado: {resultado}</p>

</div>