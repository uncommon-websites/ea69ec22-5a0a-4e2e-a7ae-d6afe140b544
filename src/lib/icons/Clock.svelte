<script lang="ts">
  type Props = {
    class?: string;
    size?: number;
  };
  
  let { class: className = "", size = 24 }: Props = $props();
</script>

<svg
  class={className}
  width={size}
  height={size}
  viewBox="0 0 24 24"
  fill="none"
  stroke="currentColor"
  stroke-width="2"
  stroke-linecap="round"
  stroke-linejoin="round"
>
  <circle cx="12" cy="12" r="10" />
  <polyline points="12,6 12,12 16,14" />
</svg>