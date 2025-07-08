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
  <path d="M20 13c0 5-3.5 7.5-8 7.5s-8-2.5-8-7.5c0-1.3.3-2.5.8-3.5L12 3l7.2 6.5c.5 1 .8 2.2.8 3.5" />
  <path d="m9 12 2 2 4-4" />
</svg>