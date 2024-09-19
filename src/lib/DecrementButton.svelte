<script>
	import { count } from '../store/counterStore.js';

	function decrement() {
		count.update((n) => n - 1);
	}
</script>

<button on:click={decrement}>Decrement</button>
