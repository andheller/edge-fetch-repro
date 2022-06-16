<script context="module">
	export async function load({ params, fetch }) {
		const res = await fetch(`https://jsonplaceholder.typicode.com/todos/1`);
		const text = await res.text();
		return {
			props: {
				text
			}
		};
	}
</script>

<script>
	export let text;
</script>

<div>{text}</div>
