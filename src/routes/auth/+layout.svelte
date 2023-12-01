<script lang="ts">

  import arrowLeft from "$lib/assets/icons/arrow-left.svg";

  const handleGoBack = () => {
    if (window.history.length > 1 && window.location.pathname !== '/') {
      window.history.back();
    } else {
      window.location.href = '/';
    }
  };

</script>

<header id="header-login">
  <div class="header-container">
    <button class="go-back-container" on:click={handleGoBack} on:keydown|preventDefault={event => event.key === 'Enter' && handleGoBack()} aria-label="voltar">
      <img src={arrowLeft} alt="Voltar" class="go-back" />
    </button>
  </div>
</header>

<slot />

<style>

  #header-login {
    width: 100%;
    height: 96px;
    padding: 29px 48px;
    display: flex;
    position: sticky;
    border-bottom: 1px solid #cecece;
    background: #fff;
  }
  .header-container {
    max-width: 1824px;
    flex: 1;
    margin: 0 auto;
    display: flex;
    align-items: center;
    /* justify-content: flex-start; */
  }

  button.go-back-container {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 52px;
    height: 52px;
    border-radius: 100%;
    border: 0;
    cursor: pointer;
    background-color: var(--theme-color-white);
  }

  button.go-back-container:hover {
    background-color: var(--theme-color-light-grey);
  }

  .go-back {
    height: 24px;
  }

  @media (max-width: 768px) {
    #header-login {
      padding: 0 16px;
    }
  }
</style>