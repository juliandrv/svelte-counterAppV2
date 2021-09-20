<script lang="ts">
  let counter: number = 5;

  const modifyCounter = (value: number): number => (counter += value);

  // const substract = (): number => counter--;

  // const add = (): void => {
  //   counter++;
  // };

  // const reset = (): void => {
  //   counter = 5;
  // };
</script>

<main>
  <h1>Counter App</h1>
  <hr />
  <h2 class={counter < 0 ? "negative" : "positive"}>Counter: {counter}</h2>
  <div>
    <button class="substract" on:click={() => modifyCounter(-1)}>-1</button>
    <button class="add" on:click={() => modifyCounter(+1)}>+1</button>
    <button class="reset" on:click={() => (counter = 5)}>Reset</button>
  </div>
</main>

<style>
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  h2 {
    font-size: 2em;
  }
  .negative {
    color: red;
  }
  .positive {
    color: inherit;
  }

  button {
    border: none;
    border-radius: 3px;
    color: #fff;
    font-weight: 800;
    padding: 10px 30px;
    cursor: pointer;
  }

  button.substract {
    background-color: #3a9aea;
  }
  button.substract:active {
    background-color: rgb(49, 132, 199);
  }

  button.add {
    background-color: #26d231;
  }
  button.add:active {
    background-color: rgb(34, 185, 44);
  }

  button.reset {
    background-color: #ff3e00;
  }
  button.reset:active {
    background-color: rgb(219, 55, 1);
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
