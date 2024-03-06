<script>
  import logo from "$lib/assets/icons/pescoujobs-logo.svg";
  import logoRetractable from "$lib/assets/icons/pescoujobs-logo-retractable.svg";
</script>

<footer>
  <div class="footer">
    <div class="footer-logo">
      <img src={logo} alt="Logo PescouJobs" class="pescoujobs-logo" />
    </div>
    <div class="footer-links">
      <ul>
        <li><a href="/dashboard">Para prestadores</a></li>
        <li><a href="/">Ajuda</a></li>
        <li><a href="/auth/register">Cadastrar</a></li>
      </ul>
    </div>
  </div>
  <div
    class="ccright"
    id="ccright"
    style="display: flex; background-color: var(--theme-color-primary);align-items: center;justify-content: center;color: var(--theme-color-white);padding: 10px 0px;font-size: 1.5vmin"
  >
    <script>
      document.getElementById("ccright").innerHTML =
        "Copyright &copy; " +
        new Date().getFullYear() +
        " - All Rights Reserved";
    </script>
  </div>

  <div class="footer-mobile">
    <nav id="mobile-menu">
      <a href="/"
        ><img
          src={logoRetractable}
          alt="Logo PescouJobs"
          class="pescoujobs-logo-retractable"
        /></a
      >
    </nav>
  </div>
</footer>

<style>
  .footer {
    display: flex;
    justify-content: space-between;
    border-top: 1px solid var(--theme-color-secondary);
    align-items: center;
    padding: 1% 10%;
    background-color: var(--theme-color-white);
    color: var(--theme-color-white);
  }

  .footer-logo {
    display: flex;
    align-items: center;
  }

  .footer-logo img {
    width: 12vmin;
  }

  .footer-links ul {
    display: flex;
    list-style: none;
  }

  .footer-links ul li {
    margin: 0 10px;
  }

  .footer-links ul li a {
    color: var(--theme-text-color-primary);
    text-decoration: none;
  }

  .footer-mobile {
    display: none;
  }

  @media (max-width: 768px) {
    .footer {
      display: none;
    }

    .footer-mobile {
      display: block;
      border-top: 1px solid var(--theme-color-white);
      background-color: var(--theme-color-primary);
      color: var(--theme-color-white);
      padding: 10px;
      text-align: center;
    }

    .footer-mobile img {
      width: 10%;
    }
  }
</style>
