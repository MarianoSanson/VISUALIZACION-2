<script>
  import * as d3 from "d3"
  export let n = 0
</script>

<div class="waffle">
  <!-- d3 range inverse -->

  {#each d3.range(0, 100) as number}
    {#if number < n}
      <div class="cuad lleno"></div>
    {:else}
      <div class="cuad vacio"></div>
    {/if}
  {/each}
</div>

<style>
  .waffle {
    display: grid;
    grid-template-columns: repeat(10, 1fr);
    grid-template-rows: repeat(10, 1fr);
    grid-auto-flow: column-reverse;
    transform: rotateX(180deg);
    width: 100%;
    height: 100%;
    gap: 1px;
    margin: 10px;
  }
  .cuad {
    font-size: 5px;
    width: 10px;
    height: 10px;
    /* border: 1px solid black; */
  }
  .vacio {
    background-color: #ddd;
  }
  .lleno {
    background-color: red;
  }
</style>
