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
	<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 13l4-4 4 4 10-10M21 3l-6 6-4-4-4 4-7 7" />
</svg>