<script>
	import Product from "../../components/product.svelte";
	import { fade } from "svelte/transition";
	
	const products = [
		{ title: "images/HILL BILLY SHIRT.png", price: 19 },
		{ title: "images/HILL BILLY SHIRT.png", price: 39 },
        { title: "images/HILL BILLY SHIRT.png", price: 39 },
        { title: "images/HILL BILLY SHIRT.png", price: 39 },
        { title: "images/HILL BILLY SHIRT.png", price: 39 },
	]
	
	let selected = null
	
	function toggle(product) {
		selected = selected == product ? null : product
	}
</script>
<body transition:fade>
	<main>
		<div class="menu-items">
	
			<div class="menu-item">
				<a href="/">
				  <img src="images/sr-log.png" alt="" class="logo-link">
				</a>
			  </div>
	
		  </div>
	
		<ul>
			{#each products as product}
				<Product {product} selected={selected == product} on:click={() => toggle(product)}/>
			{/each}
		</ul>
	</main>	
</body>

		
<style>

	
.menu-item{
        display:inline !important;
      }
	
	  .logo-link{
            height: 10vh;
          }
	
	ul {
		list-style: none;
		padding: 0;
		display: flex;
		flex-wrap: wrap;
		align-items: center;
		justify-content: center;
		gap: 2rem;
		margin: 3rem 0;
	}

</style>