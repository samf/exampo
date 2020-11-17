<script>
  import Sortable from "sortablejs";
  let num = 0;

  let allthings = new Array();
  let things = new Array();

  function newNum() {
    num += 1;
    allthings.push(num);
    things = allthings;
  }

  function makeSortable(el) {
    Sortable.create(el);
  }
</script>

<button on:click={newNum}>new item</button>
<h1>items</h1>
<ul use:makeSortable>
  {#each things as thing, index}
    <li>{thing}</li>
  {/each}
</ul>
