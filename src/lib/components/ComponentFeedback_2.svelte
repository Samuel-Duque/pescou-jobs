<script>
// @ts-nocheck

    import '../../styles.css';
    import estrelas from "$lib/assets/icons/star-avaliation.svg";
    import foto_user2 from '$lib/assets/icons/foto-user2.svg';
    import estrelas_vazias from '$lib/assets/icons/estrelas-vazias.svg'
    // @ts-ignore
    // export let id;
    



</script>

<div class="corpo-card">
    <img src={foto_user2} alt="foto-usuario" class="foto">
    <div class="texto">
        <div class="head-card">
            <span class="nome">Luan Santana</span>
            <div class="avaliacao">
                <img src={estrelas} alt="estrelas" class="estrela">
                <img src={estrelas} alt="estrelas" class="estrela">
                <img src={estrelas} alt="estrelas" class="estrela">
                <img src={estrelas} alt="estrelas" class="estrela">
                <img src={estrelas} alt="estrelas" class="estrela">
                <span class="numero-estrelas">5</span>
                <span class="divisor">|</span>
                <span class="tempo-avaliacao">Há 2 meses</span>
            </div>
        </div>
        <div class="texto-feedback">
            Marcos Antônio é um verdadeiro mago da eletricidade! Ele resolveu um problema elétrico em minha casa de forma rápida e eficaz. Estou muito satisfeita com o excelente serviço que ele prestou.
        </div>
    </div>
</div>

<style>
    .tempo-avaliacao, .divisor{
        color: var(--theme-color-dark-gray);
        text-align: right;
    }
    .avaliacao{
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 8px;
    }
    .nome{
        font-weight: 600;
    }
    .head-card{
        display: flex;
        justify-content: space-between;
    }
    .foto{
        width: 6;
        height: 6vh;
        border-radius: 50%;
    }
    .texto{
        gap: 10px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        padding: 0 12px;
    }
    .corpo-card{
        border-top: 1px solid var(--theme-color-light-gray);
        display: flex;
        flex-direction: row;
        padding: 30px 20px;
    }
    @media (max-width: 768px){
        .head-card{

            flex-direction: column;
            align-items: center;
            gap:18px;
            margin-bottom: 2vmin;
        }
        .texto{
            text-align: justify;
            justify-content: center;
        }
        .corpo-card{
            flex-direction: column;
            padding: 5vmin;
        }
        .avaliacao{
            gap:8px;
        }
        .numero-estrelas{
            display: none;
            /* margin-inline: -4px; */
        }
    }
</style>