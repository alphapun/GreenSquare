<script>
    let seacrhAppear;
    $: seacrhAppear = false;
    let searchQuery = '';
    import { fade, scale } from "svelte/transition";
    function handleSearch() {
    console.log('Search query:', searchQuery);
    // You can perform further actions with the search query, such as making an API request or filtering data.
    }
    if (seacrhAppear) {
        let val = none;
    }

  </script>
  <img
    src="src\Assets\search.svg"
    alt="search-icono"
    on:mouseenter={() => {
      seacrhAppear = !seacrhAppear;
    }} class:selected-n="{seacrhAppear}"
  />
  {#if seacrhAppear}
  <div class="search-bar" in:scale out:fade>
    <input
      type="text"
      class="search-input-n"
      placeholder="Enter search query..."
      class:search-input="{seacrhAppear}"
      bind:value={searchQuery}
      on:keydown={(event) => {
        if (event.key === 'Enter') {
          handleSearch();
        }
      }}
    />
  </div>
  {/if}


  <style>
    .selected-n{
        display: none;
    }
    img{
        height: 30px;
    }
    .search-input-n{
        display: none;
    }

    .search-input{
        font-size: 15px;
        background: rgba(217, 217, 217, 0.55);
        width: 40%;
        height: 24px;   
        border-radius: 60px;
        display: inline-block;
        padding: 5px;
        border: 1px solid #ccc;
    }
  </style>