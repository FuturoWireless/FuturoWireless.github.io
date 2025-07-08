<script lang="ts">
  import Fa from 'svelte-fa'
  import { faCircleUser } from '@fortawesome/free-solid-svg-icons'
  import '../app.css'
    import Logo from '$lib/logo.svelte'

  let { children } = $props()
</script>

<svelte:head>
  <title>Futuro Wireless</title>
  <meta
    name="description"
    content="Internet banda larga de alta qualidade para sua casa ou empresa. Conheça a Futuro Wireless."
  />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta property="og:title" content="Futuro Wireless" />
  <meta
    property="og:description"
    content="Internet banda larga de alta qualidade para sua casa ou empresa. Conheça a Futuro Wireless."
  />
  <meta property="og:image" content="/favicon.png" />
  <meta property="og:type" content="website" />
  <meta name="robots" content="index, follow" />
</svelte:head>

<header
  class="w-full h-20 flex flex-row items-center py-1 px-2 justify-between fixed bg-gray-950 shadow-md"
>
  <Logo
    class="*:fill-white h-full"
  />
  <nav></nav>
  <button
    tabindex="0"
    class="flex flex-row gap-2 items-center rounded-md pr-10 pl-8 py-2 text-white mr-3"
    onclick={() => {
      open('https://futurowireless.com.br/central_assinante_web/login', '_self')
    }}
  >
    <Fa icon={faCircleUser} />
    Entrar
  </button>
</header>

{@render children()}

<footer>
  <div class="bg-gray-950 text-white py-4 text-center">
    <p class="text-sm leading-4">
      &copy; {new Date().getFullYear()} Futuro Wireless. Todos os direitos reservados.<br
      />
      Tv. Conde de Porto Alegre, 180, Sala 02, Centro, Seberi - RS, 98380-000<br
      />
      CNPJ: 10.623.026/0001-40
    </p>
  </div>
  <!--
    Código por: Leonardo Kopeski
    github.com/leonardokopeski
  -->
</footer>
