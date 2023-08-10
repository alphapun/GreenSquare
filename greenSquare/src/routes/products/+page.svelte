<script>
  
  import Modal from '../../Components/Modal.svelte';
    import AddProduct from '../../Components/addProduct.svelte';


  let showModal = false;

  let toggleModal = () => {
    showModal = !showModal;
  };

	let products = [
    { name: 'Apple', sellername: 'Hari', price: 250, id: 1 },
    { name: 'Banana', sellername: 'Jose', price: 450, id: 2 },
    { name: 'Shirt', sellername: 'Dalin', price: 350, id: 3 }
  ];

  const handleClick = (e, id) => {
    products = products.filter(product => product.id != id);
    console.log(e);
  };

  const addProduct = (e) => {
    //console.log(e.detail);
    const product = e.detail;
    products = [product, ...products];
    showModal = false;
  };
</script>

<Modal {showModal} on:click={toggleModal}>
  <AddProduct on:addProduct={addProduct} />
</Modal>

<main>
  <button id="add" on:click={toggleModal}>Add products</button>
  <div class="gap"></div>
  <div class="product-cards">
    {#each products as product (product.id)}
      <div class="product-card">
        <h4>{product.name}</h4>
        <p>{product.price} Rs</p>
        <p>Sold By: {product.sellername}</p>
        <button id="delete" on:click={(e) => handleClick(e, product.id)}>Buy</button>
      </div>
    {:else}
      <p>There are no products to show...</p>
    {/each}
  </div>
</main>

<style>
  #delete {
    border: 2px solid #111827 ;
    background-color: #3ab37c;
    border-radius: 8px;
    padding: 5px;
    margin-top: 15px;
  }
  .gap{
    margin: 2%;
  }
  h4{
    font-weight: 900;
  }
  #add{
    border: 2px solid #111827 ;
    background-color: #3ab37c;
    border-radius: 8px;
    padding: 5px;
    font-weight: 700;
  }
  .product-card{
    border: 2px solid black ;
    padding: 10px;
  }
  .product-cards{
    display: flex;
    gap:20px 
  }
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>