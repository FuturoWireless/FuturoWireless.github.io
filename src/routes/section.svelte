<script lang="ts">
  import type { Snippet } from 'svelte'
  import type { HTMLAttributes } from 'svelte/elements'

  // ==================== Props ====================
  let {
    title,
    children,
    titleClass,
    ...other
  }: {
    title?: string
    titleClass?: string
    children: Snippet
  } & HTMLAttributes<any> = $props()
</script>

<section
  {...other}
  class="flex flex-col items-center justify-center py-10 {other.class}"
>
  <h1 class="text-4xl text-center font-semibold leading-20 text-primary-900 {titleClass}">{title}</h1>
  <div class="flex md:flex-row flex-col px-2 max-w-200 md:gap-20 gap-1">
    {@render children()}
  </div>
</section>
