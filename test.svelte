<script>
	let items = ["item 1"]
	
	export function addItem() {
		console.log("working")
		const lastItem = items[items.length -1]
		const lastItemId =  parseInt(lastItem.match(/\d+/)[0])

		const newItem = `item ${lastItemId + 1}`

		items.push(newItem)
	}
	
</script>
<ul>
{#each items as item}
	<li>
		{item}
	</li>
{/each}
</ul>

<button on:click={addItem}> Add Item </button>
