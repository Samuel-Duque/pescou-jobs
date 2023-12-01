<script lang="ts">
  import HeaderSearcher from "$lib/components/Header-Searcher.svelte";
  import arrow_right from "$lib/assets/icons/slight-arrow-right.svg";
  import ServiceCategories from "$lib/components/ServiceCategories.svelte";
  import "../../styles.css";
  import star_active from "$lib/assets/icons/star-avaliation.svg";
  import imagem_perfil from "$lib/assets/image-perfil.svg";
  import verified from "$lib/assets/icons/verified.svg";
  import pin_localizacao from "$lib/assets/icons/pin-localizacao.svg";
  import foto_perfil_grande from "$lib/assets/icons/foto-perfil-grande.svg";
  import Button from "$lib/components/Button.svelte";
  import Calendar from "$lib/components/calendar.svelte";
  import white_arrow from "$lib/assets/icons/white-arrow.svg";
  import ComponentFeedback_2 from "$lib/components/ComponentFeedback_2.svelte";
  const handleNavigateProfessionals = () => {
    window.location.href = "/profissionais";
  };
  let showCalendar = false;

</script>

<meta name="viewport" content="width=device-width, initial-scale=1.0" />

<title>Perfil</title>

<HeaderSearcher></HeaderSearcher>
<ServiceCategories />

<body>
  <div class="div-esquerda">
    <div class="head-nav">
      <div class="navbar">
        <span class="inicio">Início</span>
        <img src={arrow_right} alt="Seta p/ direita" />
        <span>Eletricistas</span>
        <img src={arrow_right} alt="Seta p/ direita" />
        <span>Eletricista1002</span>
      </div>
      <div class="profissional-procurado">
        <span class="texto-profissional"
          >Seu eletricista de confiança para iluminar e proteger.</span
        >
        <div class="avaliacao">
          <img src={star_active} alt="Estrela" />
          <span class="numero-avaliacao" style="font-weight: 600; width:auto"
            >4.9 <b style="font-weight: 400;color:#777"
              >(<b style="font-weight: 400; text-decoration-line:underline">225</b
              >)</b
            ></span
          >
        </div>
      </div>
    </div>

    <div class="container-foto-nome">
      <img src={foto_perfil_grande} alt="Foto de perfil" />
      <div class="nome-localizacao-botao">
        <div class="foto-nome-verified">
          <span class="nome-prestador">Marcos Antônio</span>
          <img src={verified} alt="Verificado" />
        </div>
        <div class="localizacao">
          <img src={pin_localizacao} alt="" />
          <div class="localizacao-texto">Imbiribeira, Recife, Pernambuco</div>
        </div>
        <div class="botao-contato">
          <Button expended text="Entre em contato comigo" type="outline" />
        </div>
      </div>
    </div>

    <div class="titulo"><span id="titulo">Eletricista Profissional</span></div>
    <div class="corpo-descricao">
      <div class="descricao-texto">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Modi quibusdam
        provident illum aut enim praesentium, aspernatur iste cum! Dolorem sunt
        labore incidunt cumque voluptatibus sapiente vitae, sequi deleniti
        accusantium quisquam. Lorem ipsum dolor sit amet consectetur adipisicing
        elit. Ratione libero, error beatae minima voluptatem, nemo deserunt
        porro odio iusto consequuntur pariatur id officia natus rem maxime
        numquam officiis corrupti aut? Lorem, ipsum dolor sit amet consectetur
        adipisicing elit. Dolor temporibus accusantium omnis, aut nemo alias
        iste blanditiis sint maiores fugiat laudantium odit saepe ratione
        quibusdam ad illum quia consectetur at! Lorem ipsum dolor sit amet
        consectetur adipisicing elit. Maxime, dicta, esse voluptatum dolores,
        minus enim reprehenderit non voluptatem tenetur at molestias iure!
        Expedita pariatur itaque nulla, unde inventore fuga in.
      </div>
    </div>
    <div class="tags-relacionadas">
      <div class="tag">
        <span id="tag_texto">Instalação elétrica residencial</span>
      </div>
      <div class="tag">
        <span id="tag_texto">Reparo de circuitos elétricos</span>
      </div>
    </div>
    <div class="botao-portfolio">
      <Button expended text="Ver portfólio" type="primary" iconRight={white_arrow} />
    </div>
    <div class="avaliacoes-texto">
      <div class="avaliacoes-texto-head"><span id="header"><h2><b>Avaliações</b></h2></span></div>
      <div class="avaliacoes-texto-body">
        <ComponentFeedback_2/>
        <ComponentFeedback_2/>
        <ComponentFeedback_2/>
        <ComponentFeedback_2/>
      </div>
    </div>
  </div>
  <div class="div-direita">
      <div class="container-agendar">
        <div class="botao1">
          <Button
            expended
            text="Pedir Orçamento"
            type="primary"
            onClick={handleNavigateProfessionals}
          />
        </div>
        <div class="botao2">
          <Button
            expended
            text="Fazer agendamento"
            type="outline"
            onClick={() => {
              showCalendar = !showCalendar;
              console.log("Botão clicado, showCalendar é", showCalendar);
            }}
          />
        </div>
      </div>
      {#if showCalendar}
        <div class="calendario">
          <Calendar />
        </div>
      {/if}
      <div class="avaliacoes">
        <h2>Avaliações</h2>
        <div class="head-avaliacoes">
          <span class="total-avaliacoes">225 avaliações desse prestador</span>
          <div class="linha-media-estrela">
            <img src={star_active} alt="Estrela" />
            <img src={star_active} alt="Estrela" />
            <img src={star_active} alt="Estrela" />
            <img src={star_active} alt="Estrela" />
            <img src={star_active} alt="Estrela" />
            4.9
          </div>
        </div>
        <div class="container-avaliacao">
          <div class="avaliacao">
            <img src={star_active} alt="Estrela" />
            <span class="numero-avaliacao" style="font-weight: 600;"
              >5 <b style="font-weight: 400;color:#777"></b></span
            >
            <div class="barra"><div class="preencher"></div></div>
            <span class="numero-avaliacoes">(174)</span>
          </div>
          <div class="avaliacao">
            <img src={star_active} alt="Estrela" />
            <span class="numero-avaliacao" style="font-weight: 600;"
              >4 <b style="font-weight: 400;color:#777"></b></span
            >
            <div class="barra">
              <div class="preencher" style="width: 11%;"></div>
            </div>
            <span class="numero-avaliacoes">(36)</span>
          </div>
          <div class="avaliacao">
            <img src={star_active} alt="Estrela" />
            <span class="numero-avaliacao" style="font-weight: 600;"
              >3 <b style="font-weight: 400;color:#777"></b></span
            >
            <div class="barra">
              <div class="preencher" style="width: 7%;"></div>
            </div>
            <span class="numero-avaliacoes">(12)</span>
          </div>
          <div class="avaliacao">
            <img src={star_active} alt="Estrela" />
            <span class="numero-avaliacao" style="font-weight: 600;"
              >2 <b style="font-weight: 400;color:#777"></b></span
            >
            <div class="barra">
              <div class="preencher" style="width: 4%;"></div>
            </div>
            <span class="numero-avaliacoes">(2)</span>
          </div>
          <div class="avaliacao">
            <img src={star_active} alt="Estrela" />
            <span class="numero-avaliacao" style="font-weight: 600;"
              >1 <b style="font-weight: 400;color:#777"> </b></span
            >
            <div class="barra">
              <div class="preencher" style="width: 1%;"></div>
            </div>
            <span class="numero-avaliacoes">(1)</span>
          </div>
        </div>
      </div>
    </div>

</body>

<style>
   
  .avaliacoes-texto-head{
    display: flex;
    padding: 10px;
  }
  .avaliacoes-texto{
    padding:20px;
  }
  .botao-portfolio{
    margin-top: 20px;
    width: 40vmin;
  }
  .avaliacao .numero-avaliacao{
    width:6px;
  }
  .numero-avaliacoes{
    font-size: 1rem;
    color: var(--theme-color-text-secondary);
    text-align: right;
    width: 50px;
  }
  .calendario {
    right: 15%;
    top: 50%;
    position: absolute;
    z-index: 1;
    display: flex;
  }
  .avaliacao > img {
    width: 20px;
  }
  .head-avaliacoes {
    display: flex;
    align-items: center;
    gap: 10px;
  }
  .linha-media-estrela {
    display: flex;
    gap: 5px;
    height: 20px;
  }
  .container-avaliacao {
    display: flex;

    flex-direction: column;
    justify-content: center;
    margin-top: 20px;

  }
  .avaliacao {
    padding: 5px;
    display: flex;
    align-items: center;
    row-gap: 10px;
    gap: 20px;
    
  }
  .preencher {
    background: var(--theme-color-secondary);
    width: 90%;
    height: 8px;
    border-radius: 999px;
  }
  .barra {
    display: flex;
    justify-content: space-between;
    background: #cecece;
    width: 60%;
    height: 9px;
    border-radius: 999px;
  }
  .avaliacoes {
    display: flex;
    position: sticky;
    top:32%;
    padding: 20px;
    flex-direction: column;
    margin-left: 5vmin;
    /* align-items: center; */
    justify-content: center;
    margin-top: 10vmin;
    margin-left: calc(10vmin);
  }
  
  .botao1,
  .botao2 {
    width: 100%;
  }
  .corpo-descricao .descricao-texto{
    font-size: 1rem;
    position: relative;
    text-align: justify;
    padding: 10px;
  }
  .container-agendar {
    display: flex;
    position: sticky;
    top:8%;
    margin-left: 23%;
    margin-top: 25%;
    gap: 20px;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    width: 60%;
    padding: 23px 19px;
    border-radius: 5px;
    border: 1px solid #cecece;
    background: #fff;
    box-shadow: 0px 2px 3px 1px rgba(0, 0, 0, 0.03);
  }
  .div-direita {

    /* border: 1px solid #ff9811; */
  }
  .div-esquerda {
    /* border: 1px solid #1dbf73; */
  }
  .corpo-descricao {
    display: grid;
    /* border: 1px solid palegreen; */
    /* width: 50%; */
    gap: 30px;
  }
  .tag {
    color: var(--theme-color-text-primary);
    border-radius: 10vmin;
    background: #eee;
    display: flex;
    padding: 10px 16px;
    align-items: center;
    gap: 10px;
  }
  .tags-relacionadas {
    display: flex;
    gap: 10px;
    padding: 20px 0px;
    /* border: #e4e5e7 1px solid; */
  }
  .titulo {
    font-weight: 600;
    font-size: 2rem;
    padding: 10px 0px;
  }
  .localizacao {
    display: flex;
    align-items: center;
    gap: 10px;
    /* border: #e4e5e7 1px solid; */
  }
  .nome-localizacao-botao {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 8px;
    /* border: #e4e5e7 1px solid; */
  }
  .foto-nome-verified {
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 1.5rem;
    font-weight: 600;
    /* border: #e4e5e7 1px solid; */
  }
  .container-foto-nome > img {
    width: 12vmin;
    border-radius: 50%;
    /* border: #e4e5e7 1px solid; */
  }
  .container-foto-nome {
    display: flex;
    align-items: center;
    width: 40%;
    justify-content: center;
    width: fit-content;
    gap: 18px;
    padding: 30px 0px;
    /* border: #4c7ee2 1px solid; */
  }
  body {
    padding: 20px 120px;
    /* background: #131313; */
    display: grid;
    grid-template-columns: 1fr 1fr;
  }
  .avaliacao {
    display: flex;
    align-items: center;
    top: 0;
    gap: 10px;
    /* border: #e4e5e7 1px solid; */
  }
  .texto-profissional {
    font-size: 2rem;
    font-weight: 600;
  }
  .profissional-procurado {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 10px;
    /* width: 60%; */

    /* border: #1dbf73 1px solid; */
  }
  .navbar {
    display: flex;
    padding: 16px 0px;
    align-items: center;
    gap: 15px;
  }
  .head-nav {
    display: flex;
    width: auto;
    /* padding: 0px 134px; */
    flex-direction: column;
    align-items: flex-start;
    gap: 23px;
  }

  @media (max-width: 1024px) {
    .calendario {
      right: 5%;
      /* top: 50%; */
      position: absolute;
      z-index: 1;
      display: flex;
    }
    .container-agendar {
      margin-top: 45%;
      margin-left: 10%;
      width: 80%;
    }
    .profissional-procurado {
      width: 100%;
      padding: 20px;
    }
    body {
      padding: 30px 30px;
    }
    .container {
      width: 100%;
      max-width: 720px;
    }
    .nome-localizacao-botao {
      padding: 10px;
    }

    @media screen and (max-width: 768px) {
      .botao-portfolio{
        margin-top: 20px;
        width: 100%;
      }
      .avaliacoes-texto-head{
        display: flex;
        padding: 10px;
        justify-content: center;
      }
      .calendario{
        margin-right: 05%;
        justify-content: center;
        border-radius: 8px;
        border: 1px solid var(--theme-border-color-primary);
      }
      .avaliacoes > h2 {
        text-align: center;
        font-size: 1.5rem;
      }
      .head-avaliacoes {
        display: flex;
        flex-direction: column;
        align-items: center;
      }
      .avaliacoes {
        margin-left: 0vmin;
        
      }
      .container-agendar {
        margin-top: 5%;
        margin-left: 0%;
        margin-bottom: -10%;
        width: 100%;
      }
      .div-direita {
        display: block;
        width: 100%;
      }
      body {
        display: block;
      }
      .container-foto-nome {
        display: flex;
        flex-direction: column;
        width: 100%;
      }
      .nome-localizacao-botao .localizacao {
        padding: 10px;
      }
      .nome-localizacao-botao .localizacao,
      .nome-localizacao-botao .foto-nome-verified,
      .nome-localizacao-botao .botao-contato {
        width: 100%;
        justify-content: center;
      }
      .nome-localizacao-botao {
        display: flex;
        flex-direction: column;
        width: 100%;
      }
      .titulo {
        font-size: 1.5rem;
        justify-content: center;
        align-items: center;
        text-align: center;
        padding: 10px;
      }
      .corpo-descricao {
        border-radius: 5px;
        padding: 10px;
        width: 100%;
        height: 200px;
        overflow-y: auto;
      }
      .corpo-descricao::-webkit-scrollbar {
        width: 5px;
      }

      .corpo-descricao::-webkit-scrollbar-track {
        background: var(--theme-color-light-gray);
        height: calc(100%-20px);
        margin: 4px;
      }

      .corpo-descricao::-webkit-scrollbar-thumb {
        background: var(--theme-color-primary);
        border-top-right-radius: 10px;
        border-bottom-right-radius: 10px;
        height: 50px;
      }

      .corpo-descricao::-webkit-scrollbar-thumb:hover {
        background: #555;
      }
      .corpo-descricao .descricao-texto {
        font-size: 1rem;
        position: static;

      }
      .tag {
        font-size: 0.8rem;
      }
      .tags-relacionadas {
        position: relative;
        text-align: center;
        flex-direction: row;
        gap: 10px;
        justify-content: center;
        align-items: center;
      }
    }
    @media screen and (max-width:480px) {
      .calendario{
        margin-right: 0%;
        justify-content: center;
        border-radius: 8px;
        border: 1px solid var(--theme-border-color-primary);
      }
    }

  }
</style>
