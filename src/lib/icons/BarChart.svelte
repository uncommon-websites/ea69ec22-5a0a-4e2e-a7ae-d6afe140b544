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
  <line x1="12" x2="12" y1="20" y2="10" />
  <line x1="18" x2="18" y1="20" y2="4" />
  <line x1="6" x2="6" y1="20" y2="16" />
</svg>