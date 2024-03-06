<script lang="ts">
  import Button from "$lib/components/Button.svelte";
  import Header from "$lib/components/Header.svelte";
  import arrowicon from "$lib/assets/icons/arrow-right.svg";
  import InputServiceLocation from "$lib/components/input-service-location.svelte";
  import backgroundImage from "$lib/assets/foto-back.png";
  import CardContador from "$lib/components/card-contador.svelte";
  import Teste from "$lib/components/teste.svelte";
  import trabalhadoresImage from "$lib/assets/trabalhadores.svg";
  import Footer from "$lib/components/Footer.svelte";
  import "aos/dist/aos.css";
  import AOS from "aos";
  import { onMount } from "svelte";

  onMount(() => {
    AOS.init();
  });

  const handleNavigateProfessionals = () => {
    window.location.href = "/profissionais";
  };
</script>

<svelte:head>
  <title>PescouJobs - Encontre Profissionais Qualificados</title>
  <meta name="description" content="Encontre profissionais Qualificados" />
</svelte:head>

<Header />

<img
  src={backgroundImage}
  alt="Logo PescouJobs"
  class="background-image-responsive"
/>

<div class="background" style="background-image: url({backgroundImage})">
  <div class="corpo">
    <div class="header-bloco">
      <div class="texto-head">
        <span>Encontre Profissionais Qualificados</span>
        <div class="subheader">
          <span
            >Busque por <b style="color: var(--theme-color-secondary)"
              >serviço</b
            >
            e <b style="color: var(--theme-color-secondary)">profissionais</b> confiáveis
            perto de você.</span
          >
        </div>
        <div class="servicelocation">
          <InputServiceLocation />
        </div>
      </div>

      <div class="button-finder">
        <Button
          iconRight={arrowicon}
          expended
          text="Buscar profissionais"
          type="primary"
          onClick={handleNavigateProfessionals}
        />
      </div>
    </div>
  </div>
</div>
<div class="corpo-inferior">
  <CardContador />
</div>
<div class="div_sobre" data-aos="fade-in" data-aos-duration="1000">
  <div class="div_sobre_esquerda">
    <h1>Sobre Nós:</h1>
    <p>
      A PescouJobs é a sua solução completa para encontrar serviços qualificados
      e confiáveis, simplificando a busca e a contratação de profissionais.
      Nossa plataforma online conecta clientes a prestadores de serviços de
      diversos segmentos, facilitando a sua vida e garantindo a qualidade do
      serviço prestado.
    </p>
  </div>
  <div class="div_sobre_direita">
    <img src={trabalhadoresImage} alt="Trabalhadores" width="60%" />
  </div>
</div>
<Footer />

<style>
  .div_sobre_direita {
    display: flex;
    width: 50%;
    justify-content: center;
  }

  .div_sobre_esquerda p {
    display: block;
    font-size: 1.5rem;
    font-weight: 400;
    line-height: 2.5rem;
    text-align: justify;
  }
  .div_sobre_esquerda h1 {
    /* color: var(--theme-color-primary); */
    font-size: 3rem;
    font-weight: 600;
    margin-bottom: 32px;
    border-bottom: 3px solid var(--theme-color-secondary);
    display: inline-block;
  }
  .div_sobre_esquerda {
    width: 50%;
    padding: 0px 50px;
    /* background-color: var(--theme-color-secondary); */
  }

  .div_sobre {
    gap: 30px;
    display: flex;
    padding: 80px;
    justify-content: space-evenly;
  }
  .corpo-inferior {
    display: flex;
    justify-content: center;
    margin-top: -70px;
  }
  .subheader {
    margin-top: 16px;
    margin-bottom: 24px;
    color: #787878;
    font-size: 1rem;
    font-weight: 400;
  }

  .background-image-responsive {
    display: none;
  }

  .header-bloco {
    width: 100%;
  }

  div.texto-head > span {
    font-size: 2.5rem;
    font-weight: 600;
    line-height: 3.2rem;
    color: var(--theme-color-secondary);
  }
  .corpo {
    display: flex;
    max-width: 680px;
    padding: 48px 32px;
    flex-direction: column;
    align-items: flex-start;
    background-color: #ffffff;
    border-radius: 5px;
    box-shadow:
      0 4px 8px 0 rgba(0, 0, 0, 0.2),
      0 6px 20px 0 rgba(0, 0, 0, 0.19);
  }
  .background {
    width: 100%;
    /* background-image: url({backgroundImage}); */
    padding: 80px 100px 100px 80px;
    /* background-position: -25vw; */
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
  }
  /* .servicelocation {
    margin-left: -20px;
  } */

  @media (max-width: 1200px) {
    .div_sobre {
      padding: 40px;
    }
  }
  @media (max-width: 900px) {
    .div_sobre_direita {
      display: none;
    }
    .div_sobre_esquerda {
      width: 100%;
      padding: 0px;
    }
    .div_sobre {
      padding: 40px;
    }
    .background-image-responsive {
      display: block;
      width: 100%;
      height: 350px;
      object-fit: cover;
    }
    .background {
      padding: 0px;
      background-image: none !important;
    }

    .corpo {
      /* width: 100%; */
      border-radius: 0px;
      box-shadow: none;
      padding: 24px 16px;
    }
    .corpo-inferior {
      margin-top: 0px;
    }
  }

  @media (max-width: 768px) {
    .div_sobre {
      padding: 40px 20px;
    }

    .div_sobre_esquerda h1 {
      display: flex;
      justify-content: center;
      border-bottom: none;
      align-items: center;
      padding: -70px;
      font-size: 2.5rem;
    }
    .div_sobre_esquerda p {
      padding: 0px;
      font-size: 1rem;
      line-height: normal;
    }
    .background-image-responsive {
      display: block;
      width: 100%;
      height: 250px;
      object-fit: cover;
    }

    div.texto-head > span {
      font-size: 2rem;
      line-height: 2.7rem;
    }

    .background {
      padding: 0px;
      background-image: none !important;
    }

    .corpo {
      /* width: 100%; */
      border-radius: 0px;
      box-shadow: none;
    }
  }
</style>
