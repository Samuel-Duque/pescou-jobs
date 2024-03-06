<script>
  import '../../styles.css';

</script>

<body>
  <div class="submenu-perfil">
    <div class="submenu-perfil__item">
      <a href="/perfil">Perfil</a>
    </div>
    <div class="submenu-perfil__item">
      <a href="/perfil/seguranca">Segurança</a>
    </div>
    <div class="submenu-perfil__item">
      <a href="/perfil/configuracoes">Configurações</a>
    </div>
    <div class="submenu-perfil__item">
      <a href="/perfil/ajuda">Ajuda</a>
    </div>
  </div>
</body>

<style>
  .submenu-perfil {
    display: flex;
    flex-direction: column;
    position: absolute;
    top: 60px;
    right: 0;
    width: 200px;
    z-index: 3;
    background-color: var(--theme-white-color);
    border-radius: 10px;
    box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.2);
  }

  .submenu-perfil__item:first-child {
    padding: 8px 16px;
    background-color: white;
    border-radius: 8px 8px 0 0;
    border-bottom: 1px solid var(--theme-border-color-primary);
  }
  .submenu-perfil__item {
    padding: 8px 16px;
    border-bottom: 1px solid var(--theme-border-color-primary);
  }

  .submenu-perfil__item:last-child {
    border-bottom: none;
    border-radius: 8px;
  }

  .submenu-perfil__item a {
    color: var(--theme-text-color-primary);
    border-radius: 10px;

    text-decoration: none;
  }

  .submenu-perfil__item a:hover {
    color: var(--theme-text-color-secondary);
  }
</style>