<script>
    import { createEventDispatcher } from 'svelte';
  
    let dispatch = createEventDispatcher();
    let name;
    let sellername;
    let price;
  
    const handleSubmit = () => {
      const product = {
        name, 
        sellername,
        price, 
        id: Math.random()  
      }
      dispatch('addProduct', product);
    };
  </script>
  
  <form on:submit|preventDefault={handleSubmit}>
    <input type="text" placeholder='name of the product' bind:value={name}>
    <input type="number" placeholder='price' bind:value={price}>
    <input type="text" placeholder='seller Name' bind:value={sellername}>
    <button>Add Product</button>
  </form>

  <style>
    form{
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      gap: 30px;
      padding: 30px;
    }
    input{
      border: 2px solid #111827 ;
      border-radius: 3px;
      padding: 3px 10px;
    }
    button{
      border: 2px solid #111827 ;
      background-color: #3ab37c;
      border-radius: 8px;
      padding: 5px;
      margin-top: 15px;
    }
  </style>