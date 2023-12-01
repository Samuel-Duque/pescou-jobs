<script>
  import { onMount } from 'svelte';
  import '../../../styles.css'
  import Header from '$lib/components/Header.svelte';
  let data = {
    name: '',
    address: '',
    complement: '',
    email: '',
    addressConfirmation: '',
    cpf: '',
    dob: '',
    phoneNumber: '',
    password: '',
    confirmPassword: ''
  };

  let isPageValid = false;

  const validatePage = () => {
    isPageValid = Object.values(data).every(value => value.trim() !== '');
    isPageValid = isPageValid && (data.address === data.addressConfirmation);
    isPageValid = isPageValid && (data.password === data.confirmPassword);
  };

  onMount(() => {
    validatePage();
  });
</script>

<!-- <Header /> -->
<main>
  <section>
    <div class="step-indicator">
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
    </div>

    <h2>Torne-se um dos nossos melhores prestadores de serviços!</h2>

    <div class="photo-upload-container">
      <div class="photo-upload-circle">
        <!-- Ícone de câmera fornecido -->
        <svg xmlns="http://www.w3.org/2000/svg" width="25" height="30" fill="currentColor" class="bi bi-camera" viewBox="0 0 16 16">
          <path d="M15 12a1 1 0 0 1-1 1H2a1 1 0 0 1-1-1V6a1 1 0 0 1 1-1h1.172a3 3 0 0 0 2.12-.879l.83-.828A1 1 0 0 1 6.827 3h2.344a1 1 0 0 1 .707.293l.828.828A3 3 0 0 0 12.828 5H14a1 1 0 0 1 1 1zM2 4a2 2 0 0 0-2 2v6a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V6a2 2 0 0 0-2-2h-1.172a2 2 0 0 1-1.414-.586l-.828-.828A2 2 0 0 0 9.172 2H6.828a2 2 0 0 0-1.414.586l-.828.828A2 2 0 0 1 3.172 4z"/>
          <path d="M8 11a2.5 2.5 0 1 1 0-5 2.5 2.5 0 0 1 0 5m0 1a3.5 3.5 0 1 0 0-7 3.5 3.5 0 0 0 0 7M3 6.5a.5.5 0 1 1-1 0 .5.5 0 0 1 1 0"/>
        </svg>
      </div>
      <span class="photo-upload-text">Faça o upload da sua foto</span>
    </div>
        
    <div class="question-grid">
      <div class="question-cell">
        <label for="name">
          <span class="question-label">Nome:</span>
        </label>
        <input type="text" id="name" bind:value={data.name} />
        <span class="question-text">Digite seu nome e sobrenome</span>
      </div>

      <div class="question-cell">
        <label for="address">
          <span class="question-label">Endereço:</span>
        </label>
        <input type="text" id="address" bind:value={data.address} />
        <span class="question-text">Digite seu endereço</span>
      </div>

      <div class="question-cell">
        <label for="complement">
          <span class="question-label">Complemento:</span>
        </label>
        <input type="text" id="complement" bind:value={data.complement} />
                <span class="question-text">Digite Complemento</span>
      </div>

      <div class="question-cell">
        <label for="email">
          <span class="question-label">E-mail:</span>
        </label>
        <input type="email" id="email" bind:value={data.email} />
                <span class="question-text">Digite seu e-mail</span>
      </div>

       <div class="question-cell">
        <label for="address">
          <span class="question-label">Endereço:</span>
        </label>
        <input type="text" id="address" bind:value={data.address} />
                 <span class="question-text">Digite seu e-mail novamente</span>
      </div>


      <div class="question-cell">
        <label for="cpf">
          <span class="question-label">CPF:</span>
        </label>
        <input type="text" id="cpf" bind:value={data.cpf} />
                <span class="question-text">Digite seu CPF</span>
      </div>

      <div class="question-cell">
        <label for="dob">
          <span class="question-label">Data de Nascimento:</span>
        </label>
        <input type="text" id="dob" bind:value={data.dob} />
                <span class="question-text">DD/MM/AAAA</span>
      </div>

      <div class="question-cell">
        <label for="phoneNumber">
          <span class="question-label">Número de Telefone:</span>
        </label>
        <input type="text" id="phoneNumber" bind:value={data.phoneNumber} />
                <span class="question-text">Digite seu celular</span>
      </div>

      <div class="question-cell">
        <label for="password">
          <span class="question-label">Senha:</span>
        </label>
        <input type="password" id="password" bind:value={data.password} />
                <span class="question-text">Digite sua senha</span>
      </div>

      <div class="question-cell">
        <label for="confirmPassword">
          <span class="question-label">Confirmar Senha:</span>
        </label>
        <input type="password" id="confirmPassword" bind:value={data.confirmPassword} />
                <span class="question-text">Digite sua senha novamente</span>
      </div>
    </div>

    <a href="fornecedor_register/Page2"><button>Próximo</button></a>
  </section>

  {#if isPageValid}
    <p>Todas as informações foram preenchidas corretamente. Agora você pode avançar para a próxima etapa.</p>
  {/if}
</main>

<style>
  main {
    text-align: center;
    max-width: 537px; 
    margin: 50px auto;
    position: relative;
  }

  .step-indicator {
    display: flex;
    align-items: center;
    justify-content: space-between;
    position: absolute;
    top: 0;
    width: 160%;
    padding: 1 20px;
  }

  .step-item {
  width: 40px;
  height: 20px;
  border-radius: 50%;
  background-color: grey;
    }

    .personal-data {
      background-color: black;
    }

    .services-offered {
      background-color: grey;
    }

    .completed {
      background-color: grey;
        }

  .step-indicator {
      display: flex;
      align-items: center;
      justify-content: space-between;
      position: absolute;
      top: 0;
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
    
    .step-line {
      height: 1px;
      width: calc(10% - 40px);
      background-color: #CECECE;
      flex-grow: 1;
      margin: 0 20px;
    }

  section {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 3em;
    position: relative;
  }

  h2 {
    font-family: 'Poppins', sans-serif;
    font-size: 18px;
    font-weight: 400;
        margin-top: 8em;
    margin-bottom: 10em;
    position: relative;
    z-index: 3;
  }

  .question-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 4em;
    justify-content: center;
  }

  label {
    margin-bottom: 0.5em;
  }

  .question-label {
    font-family: 'Poppins', sans-serif;
    font-size: 14px;
    font-weight: 400;
    line-height: 21px;
    letter-spacing: 0em;
    text-align: left;
  }

    .question-cell {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
  }
    
  input {
    width: 400px;
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
    margin-top: 1em;
    cursor: pointer;
  }

    .question-text {
    font-family: 'Poppins', sans-serif;
    font-size: 12px;
    color: #777;
    margin-top: 0.5em;
  }
    
  .photo-upload-container {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: flex-end;
    margin-top: -160px;
    margin-left: -700px;
  }

  .photo-upload-circle {
    width: 90px;
    height: 90px;
    border-radius: 50%;
    background-color: #D9D9D9;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .photo-upload-text {
    font-family: 'Poppins', sans-serif;
    font-size: 12px;
    color: #000000;
    margin-left: 10px;
  }
    
</style>
