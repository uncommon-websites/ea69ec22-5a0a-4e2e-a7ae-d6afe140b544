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
	<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="m7 17 10-10M17 7H7v10" />
</svg>