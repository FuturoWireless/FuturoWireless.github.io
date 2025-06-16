<script>
  import {
    faWhatsapp,
    faFacebook,
    faInstagram
  } from '@fortawesome/free-brands-svg-icons'
  import { faEnvelope } from '@fortawesome/free-solid-svg-icons'
  import Fa from 'svelte-fa'
</script>

<main class="pt-20">
  <section
    id="banner"
    class="bg-linear-to-br from-primary-600 to-primary-800 w-full h-96 flex flex-row items-center px-2"
  >
    <img
      src="/pictures/mulher-telefone.png"
      alt="Imagem de cabeçalho da Landing Page. Mulher segurando um celular e sorrindo, vestindo uma camiseta marrom e calça jeans, com o fundo azul."
      class="h-full grow object-contain object-center hidden md:block"
    />

    <div class="text-white grow">
      <h1 class="text-5xl font-bold mb-4">Futuro Wireless</h1>
      <p class="text-xl mb-4">
        Conectando você ao futuro com internet de alta qualidade e
        confiabilidade.
      </p>
      <div id="buttons" class="flex md:flex-row flex-col gap-4">
        <button
          class="bg-white text-primary-800 px-6 py-3 rounded-lg font-semibold hover:bg-gray-200 transition-colors"
          onclick={() => {
            open(
              'https://wa.me/555537461115?text=Olá!%20Gostaria%20de%20saber%20mais%20sobre%20os%20planos%20de%20internet.',
              '_blank'
            )
          }}
        >
          Consulte a disponibilidade
        </button>
        <button
          class="bg-white/20 text-white px-6 py-3 rounded-lg font-semibold hover:bg-white/30 hover:underline transition-colors"
          onclick={() => {
            open(
              'https://futurowireless.com.br/central_assinante_web/login',
              '_self'
            )
          }}
        >
          Acesse sua conta
        </button>
      </div>
    </div>
  </section>
  <section class="flex flex-col items-center">
    <h1 class="text-4xl text-center font-semibold leading-20">Quem Somos?</h1>
    <div class="flex md:flex-row flex-col px-2 max-w-200 md:gap-20 gap-1">
      <img
        src="/pictures/predio.jpg"
        alt="Predio da Futuro Wireless"
        class="h-100 object-cover"
      />
      <p>
        A Futuro Wireless é uma provedora de internet que se destaca por oferecer
        serviços de alta qualidade e confiabilidade.<br /><br />
        Com uma equipe dedicada e tecnologia de ponta, garantimos conexões rápidas
        e estáveis para nossos clientes.
        <br />Estamos comprometidos em conectar você ao futuro, proporcionando
        uma experiência de internet excepcional. <br />Seja para uso residencial
        ou empresarial, a Futuro Wireless é a escolha certa para quem busca
        excelência em conectividade. <br />
        Nossa missão é levar internet de alta qualidade a todos, com um atendimento
        personalizado e soluções que atendam às <b>suas</b> necessidades. <br />
        <br />
        Junte-se a nós e descubra como a Futuro Wireless pode <b>transformar</b>
        sua experiência online!
      </p>
    </div>
  </section>
  <section
    class="bg-primary-700 mt-10 pb-10 text-white flex flex-col items-center"
  >
    <h1 class="text-4xl text-center font-semibold leading-20">Contato</h1>
    <div class="flex md:flex-row flex-col px-40 md:gap-20 gap-1">
      <iframe
        title="Google Maps"
        class="w-80 h-80 shadow-md border"
        frameborder="0"
        src="https://www.google.com/maps/embed/v1/place?q=Futuro+Wireless+-+Avenida+General+Flôres+da+Cunha+-+Centro,+Seberi+-+RS,+Brasil&key=AIzaSyBFw0Qbyq9zTFTd-tUY6dZWTgaQzuU17R8"
      ></iframe>
      <div class="flex flex-col">
        <p class="mb-4">
          Você pode entrar em contato conosco através dos seguintes canais:
        </p>
        <p class="flex flex-row items-center gap-2">
          <Fa icon={faWhatsapp} />
          <a href="https://wa.me/555537461115">(55) 3746-1115</a>
        </p>
        <p class="flex flex-row items-center gap-2">
          <Fa icon={faWhatsapp} />
          <a href="https://wa.me/555537462075">(55) 3746-2075</a>
        </p>
        <p class="flex flex-row items-center gap-2">
          <Fa icon={faWhatsapp} />
          <a href="https://wa.me/5555996004736">(55) 9 9600-4736</a>
        </p>
        <p class="flex flex-row items-center gap-2">
          <Fa icon={faFacebook} />
          <a href="https://www.facebook.com/futurowireless">/futurowireless</a>
        </p>
        <p class="flex flex-row items-center gap-2">
          <Fa icon={faInstagram} />
          <a href="https://www.instagram.com/futurowireless">@futurowireless</a>
        </p>
        <p class="flex flex-row items-center gap-2">
          <Fa icon={faEnvelope} />
          <a href="mailto:comercial@futurowireless.com.br"
            >comercial@futurowireless.com.br</a
          >
        </p>
        <p class="mt-4">Nosso horário de atendimento é:</p>
        <p>Seg-Sex: das 08:00 às 12:00 e das 13:30 às 18:00</p>
        <p>Sab: das 08:00 às 12:00</p>
      </div>
    </div>
  </section>
</main>
