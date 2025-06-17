<script lang="ts">
  import type { Snippet } from 'svelte'
  import { onMount } from 'svelte'

  // ==================== Props ====================
  let {
    children
  }: {
    children: Snippet
  } = $props()

  // ==================== State ====================
  let section = $state<HTMLElement>()
  let carouselIndex = $state(0)

  // ==================== Lifecycle ================
  onMount(() => {
    setInterval(() => {
      carouselIndex += 1
      if (section && carouselIndex >= section.children.length) {
        carouselIndex = 0
      }
      update()
    }, 5000)
  })

  // ==================== Functions ================
  function update() {
    section!.scrollTo({
      left: section!.clientWidth * carouselIndex,
      behavior: 'smooth'
    })
  }
</script>

<section
  class="flex flex-row *:w-full *:shrink-0 overflow-hidden"
  bind:this={section}
>
  {@render children()}
  {carouselIndex}
</section>
