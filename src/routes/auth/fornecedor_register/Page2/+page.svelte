<script>
    import { onMount } from 'svelte';
  
    let data = {
      serviceDescription: '',
      aboutYouAndQuality: '',
      profession: '',
      servicesOffered: '',
      linkedIn: '',
      portfolio: '',
      github: ''
    };
  
    let isPageValid = false;
  
    const validatePage = () => {
      isPageValid = Object.values(data).every(value => value.trim() !== '');
    };
  
    onMount(() => {
      validatePage();
    });
  </script>
  
  <main>
    <section class="step-indicator">
      <div class="step-item-container">
        <div class="step-text">Dados pessoais</div>
        <div class="step-item personal-data"></div>
      </div>
      <div class="step-line"></div>
      <div class="step-item-container">
        <div class="step-text">Serviços oferecidos</div>
        <div class="step-item services-offered"></div>
      </div>
      <div class="step-line"></div>
      <div class="step-item-container">
        <div class="step-text">Concluído</div>
        <div class="step-item completed"></div>
      </div>
    </section>
  
    <h2>Anuncie seus serviços e alavanque sua carreira!</h2>
  
    <div class="question-grid">
      <div class="question-cell">
        <label for="serviceDescription">
          <span class="question-label">Seu serviço em uma frase:</span>
        </label>
        <input type="text" id="serviceDescription" bind:value={data.serviceDescription} />
        <span class="question-text">Defina seu serviço em uma frase</span>
      </div>
  
      <div class="question-cell">
        <label for="aboutYouAndQuality">
          <span class="question-label">Sobre você e qualidade do serviço:</span>
        </label>
        <input type="text" id="aboutYouAndQuality" bind:value={data.aboutYouAndQuality} />
        <span class="question-text">Fale sobre você e sobre seus serviços</span>
      </div>
  
      <div class="question-cell">
        <label for="profession">
          <span class="question-label">Profissão:</span>
        </label>
        <input type="text" id="profession" bind:value={data.profession} />
        <span class="question-text">Digite sua profissão</span>
      </div>
  
      <div class="question-cell">
        <label for="servicesOffered">
          <span class="question-label">Quais serviços irá oferecer:</span>
        </label>
        <input type="text" id="servicesOffered" bind:value={data.servicesOffered} />
        <span class="question-text">Escolha os serviços que irá oferecer</span>
      </div>
  
      <div class="question-cell">
        <label for="linkedIn">
          <span class="question-label">LinkedIn:</span>
        </label>
        <input type="text" id="linkedIn" bind:value={data.linkedIn} />
        <span class="question-text">Link para o seu LinkedIn</span>
      </div>
  
      <div class="question-cell">
        <label for="portfolio">
          <span class="question-label">Portfólio:</span>
        </label>
        <input type="text" id="portfolio" bind:value={data.portfolio} />
        <span class="question-text">Link para o seu portfólio</span>
      </div>
  
      <div class="question-cell">
        <label for="github">
          <span class="question-label">Github:</span>
        </label>
        <input type="text" id="github" bind:value={data.github} />
        <span class="question-text">Link para o seu github</span>
      </div>
    </div>
  
    <button on:click={validatePage}>Próximo</button>
  
    {#if isPageValid}
      <p>Todas as informações foram preenchidas corretamente. Agora você pode avançar para a próxima etapa.</p>
    {/if}
  </main>
  
  <style>
    main {
      text-align: center;
      max-width: 537px;
      margin: 50px auto;
    }
  
    .step-indicator {
      display: flex;
      align-items: center;
      justify-content: space-between;
      /* position: absolute; */
      margin: 0px 0px 0px -170px;
      width: 160%;
      padding: 1em 20px;
    }
  
    .step-item-container {
      display: flex;
      flex-direction: column;
      align-items: center;
      margin-bottom: 1em;
    }
  
    .step-text {
      font-family: 'Poppins', sans-serif;
      font-size: 14px;
      font-weight: 400;
      text-align: center;
      margin-bottom: 0.5em;
    }
  
    .step-item {
      width: 30px;
      height: 30px;
      border-radius: 50%;
    }
  
    .personal-data {
      background-color: grey;
    }
  
    .services-offered {
      background-color: black;
    }
  
    .completed {
      background-color: grey;
    }
  
    .step-line {
      height: 1px;
      width: calc(33.33% - 40px);
      background-color: #CECECE;
      flex-grow: 1;
      margin: 0 20px;
    }
  
    .question-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 6em;
      justify-content: center;
    }
  
    .question-cell {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      justify-content: flex-start;
      margin-bottom: 1em;
      max-width: 440px;
    }
  
    input{
      width: 440px;
      height: 50px;
      border: 2px solid #ccc;
      border-radius: 2px;
      padding: 1em;
      box-sizing: border-box;
    }
  
    button {
      width: 626px;
      height: 50px;
      border-radius: 10px;
      background-color: black;
      color: white;
      cursor: pointer;
    }
  
    .question-text {
      font-family: 'Poppins', sans-serif;
      font-size: 13px;
      color: #777;
      margin-top: 0.1em;
    }
  
    h2 {
      font-family: 'Poppins', sans-serif;
      font-size: 18px;
      font-weight: 400;
      margin-top: 1em;
      margin-bottom: 2em;
    }
  </style>