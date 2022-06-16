<script context="module">
	export async function load({ params, fetch }) {
		const res = await fetch(
			`https://api.stockanalysis.com/wp-json/sa/info?s=${params.ticker}&t=stocks`
		);
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
