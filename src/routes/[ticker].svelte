<script context="module">
	export async function load({ params, fetch }) {
		const res = await fetch(`https://jsonplaceholder.typicode.com/todos/1`);
		const json = await res.json();
		return {
			props: {
				json
			}
		};
	}
</script>

<script>
	export let json;
</script>

<div>{JSON.stringify(json)}</div>
