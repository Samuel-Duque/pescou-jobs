<script lang='ts'>
  import logo from "$lib/assets/icons/pescoujobs-logo.svg";
  import logoRetractable from "$lib/assets/icons/pescoujobs-logo-retractable.svg";
  import Button from "./Button.svelte";
  import account from "$lib/assets/icons/account.svg";
  import SearchBar from "./SearchBar.svelte";
  import SearchBarLocation from "./SearchBar-Location.svelte";
  import arrow_left from "$lib/assets/icons/arrow-left.svg";  
  import notification_bell from "$lib/assets/icons/notification-bell.svg";
  import imagem_perfil from "$lib/assets/icons/imagem-perfil2.svg";
  import help_icon from "$lib/assets/icons/help-icon.svg";
  import messages_icon from "$lib/assets/icons/messages-mail.svg";
  

  const handleNavigateLogin = () => {
    window.location.href = "/auth/login";
  };

</script>

<header>
  <!-- <img src={logoRetractable} alt="Logo PescouJobs" class="pescoujobs-logo-retractable"/> -->
  <nav id="desktop-menu">
    <div class="search-bar">
      <a href="/" ><img src={arrow_left} alt="Seta Esquerda" class="arrowleft"></a>
      <a href="/"><img src={logo} alt="Logo PescouJobs" class="pescoujobs-logo" /></a>
    </div>

    <div class="container-nav">
      <ul>
        
        <li><img src={notification_bell} alt=""></li>
        <li><img src={messages_icon} alt=""></li>
        <li><img src={help_icon} alt=""></li>

      </ul>
        <img src={imagem_perfil} alt="" style="height: 50px;width:50px" class="foto">
    </div>
    
  </nav>
  <nav id="mobile-menu">
    <img src={logoRetractable} alt="Logo PescouJobs" class="pescoujobs-logo-retractable" />
  </nav>
</header>

<style>
  .foto{
    border-radius: 50%;
    border: 1.5px solid var(--theme-text-color-primary);
  }
  .arrowleft{
    height: 42px;
    width: 42px;
    padding: 8px;
    background-color: var(--theme-background-color-primary);
    transition: background-color 0.3s;
    border-radius: 8px;
  }
  .arrowleft:hover{
    border-radius: 8px;
    background-color: var(--theme-border-color-primary);
  }

  .search-bar{
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 30px;
  }
  header {
    border-bottom: 1px solid var(--theme-border-color-primary);
  }

  nav {
    height: 96px;
    padding: 0 48px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  #mobile-menu {
    display: none;
  }

  ul {
    display: flex;
    margin-right: 24px;
    gap:5px;
  }
  li {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 42px;
    height: 42px;
    border-radius: 8px;
    list-style: none;
    position: relative; 
    transition: background-color 0.3s; 
  }

  li:hover {
    border-radius: 8px;
    background-color: var(--theme-border-color-primary);
  }
  

  .container-nav {
    display: flex;
    align-items: center;
  }
  .pescoujobs-logo,
  .pescoujobs-logo-retractable {
    height: 40px;
    object-fit: contain;
  }

  .pescoujobs-logo-retractable {
    display: none;
  }
  a {
    text-decoration: none;
    color: var(--theme-text-color-primary);
    font-size: 0.9rem;
    font-weight: 500;
  }

  @media (max-width: 768px) {
    nav {
      padding: 0 24px;
    }

    .pescoujobs-logo {
      height: 32px;
    }
  }

    @media (max-width: 480px) {
        header{
            padding: 0 16px;
            justify-content: center;
        }

        #desktop-menu{
            display: none;
        }

        #mobile-menu{
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .pescoujobs-logo-retractable {
            display: block;
        }
    }
    @media (max-width: 380px) {
        header{
            padding: 0 16px;
            justify-content: center;
            border: 1px solid red;
            width: 100%;
          }
          
          #desktop-menu{
            display: none;
        }

        #mobile-menu{
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .pescoujobs-logo-retractable {
            display: block;
        }
    }
</style>
