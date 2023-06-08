<script>

    import { fade } from "svelte/transition";
    export let visible = true;
    let seacrhAppear;
    $: seacrhAppear = false;
    let searchQuery = '';

    function handleSearch() {
    console.log('Search query:', searchQuery);
    // You can perform further actions with the search query, such as making an API request or filtering data.
    }

  </script>

  <img
    src="src\Assets\search.svg"
    alt="search-icono"
    on:mouseenter={() => {
      seacrhAppear = !seacrhAppear;
    }} class:selected-n="{seacrhAppear}"
  />
  {#if visible}
    {#if seacrhAppear}
    <div class="search-bar" transition:fade>
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
        color: black;
        background: #d2efe4;
        width: 400px;
        height: 24px;   
        border-radius: 60px;
        display: block;
        padding: 5px;
        border: 1px solid #ccc;
    }
  </style>