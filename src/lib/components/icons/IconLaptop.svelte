<script lang="ts">
	let { class: className = "size-4", ...props } = $props();
</script>

<svg
	{...props}
	class={className}
	fill="none"
	stroke="currentColor"
	viewBox="0 0 24 24"
	xmlns="http://www.w3.org/2000/svg"
>
	<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M20 16V7a2 2 0 00-2-2H6a2 2 0 00-2 2v9m16 0v1a2 2 0 01-2 2H6a2 2 0 01-2-2v-1m16 0H4" />
</svg>