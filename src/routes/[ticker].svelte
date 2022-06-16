<script context="module">
	export async function load({ params, fetch }) {
		const res = await fetch(`https://api.stockanalysis.com/wp-json/sa/info?s=AAPL&t=stocks`);
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
