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
  <path d="M16 21v-2a4 4 0 0 0-4-4H6a4 4 0 0 0-4 4v2" />
  <circle cx="9" cy="7" r="4" />
  <path d="m22 21-2-2" />
  <path d="m16 16 2 2" />
  <circle cx="20" cy="8" r="3" />
</svg>