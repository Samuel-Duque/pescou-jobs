<script>
// @ts-nocheck

    import '../../styles.css';
    import foto_user from '$lib/assets/icons/foto-user.svg';
    import estrelas from '$lib/assets/icons/estrelas.svg';
    import estrelas_vazias from '$lib/assets/icons/estrelas-vazias.svg'
    // @ts-ignore
    export let id;
    



</script>

<div class="corpo-card" class:corpo-feedback-impar={id % 2 === 1}>
    <img src={foto_user} alt="foto-usuario" class="foto">
    <div class="texto">
        <div class="head-card">
            <span class="nome">Luan Santana</span>
            <div class="avaliacao">
                <img src={estrelas} alt="estrelas" class="estrela">
                <img src={estrelas} alt="estrelas" class="estrela">
                <img src={estrelas} alt="estrelas" class="estrela">
                <img src={estrelas} alt="estrelas" class="estrela">
                <img src={estrelas_vazias} alt="estrelas" class="estrela">
            </div>
        </div>
        <div class="texto-feedback">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque omnis, vitae quia mollitia est temporibus quo earum id. Vitae quo excepturi consequuntur unde velit error mollitia ipsam officiis eum nulla!
        </div>
    </div>
</div>

<style>
    .corpo-feedback-impar{
        background: rgba(214, 214, 255, 0.50);
        
        }
    .nome{
        font-weight: 600;
    }
    .head-card{
        display: flex;
        justify-content: space-between;
    }
    .foto{
        width: 10vw;
        height: 10vh;
        border-radius: 50%;
    }
    .texto{
        gap: 10px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        padding: 0 20px;
    }
    .corpo-card{
        border: 1px solid var(--theme-color-light-gray);
        display: flex;
        flex-direction: row;
        padding: 40px;
    }
</style>