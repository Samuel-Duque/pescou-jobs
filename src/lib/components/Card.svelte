<script>
    import '../../styles.css';
    import imagem_perfil from '$lib/assets/image-perfil.svg';
    import verified from '$lib/assets/icons/verified.svg';
    import banner from '$lib/assets/foto-banner.svg';
    import estrela from '$lib/assets/icons/star-avaliation.svg';
    import pin_localizao from '$lib/assets/icons/pin-localizacao.svg'
</script>


<div class="corpo-card">
    <div class="imagem-banner">
        <img src={banner} alt="Banner" class="imagem-banner2">
    </div>
    <div class="head-verified">
        <img src={imagem_perfil} alt="Foto de perfil">
        <div class="nome-verified">
            <span class="nome-prestador">Marcos Antônio</span>
            <img src={verified} alt="Verificado">
        </div>
    </div>
    <span class="descricao-prestador">
        Seu eletricista de confiança para iluminar e proteger.
    </span>
    <div class="avaliacao">
        <img src={estrela} alt="Estrela">
        <span class="numero-avaliacao" style="font-weight: 600;">4.5 <b style="font-weight: 400;color:#777">(<b style="font-weight: 400; text-decoration-line:underline">5</b>)</b></span>
    </div>
    <div class="tag_area_price">
        <div class="tag_area">
            <span style="font-size:0.875rem; font-weight:600">Eletricista</span>
        </div>
        <span style="font-weight: 600;">A partir de R$ 50</span>
    </div>
    <div class="localizacao">
        <img src={pin_localizao} alt="Pin Localização" style="margin-right: 13px;">
        <span class="localizacao-nome">Imbiribeira, Recife, Pernambuco</span>
    </div>
</div>

<style>
    .imagem-banner2,.imagem-banner{
        width: 100%;
    }

    .localizacao-nome{
        font-weight: 600;
    }
    .localizacao{
        display: flex;
    }
    .tag_area{
        display: flex;
        padding: 4px 16px;
        align-items: center;
        gap: 10px;
        border-radius: 8px;
        background: #D9D9D9;
    }
    .tag_area_price{
        padding-bottom: 20px;
        border-bottom: 1px solid var(--theme-color-light-gray);
        display: flex;
        justify-content: space-between;
        align-items: flex-start;
        align-self: stretch;
    }
    .avaliacao{
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 11px;
    }
    .descricao-prestador{
        color: #777;
        font-weight: 400;
    }
    .nome-prestador{
        color: #1E1E1E;
        font-size: 1.125rem;
        font-weight: 600;
     }
    .nome-verified{
        display: flex;
        align-items: center;
        gap: 5px;
    }
    .head-verified{
        display: flex;
        align-items: center;
        gap: 8px;
        align-self: stretch;
    }
    .corpo-card{
        display: flex;
        width: 100%;
        padding: 2vmin 2vmin;
        flex-direction: column;
        justify-content: center;
        align-items: flex-start;
        gap: 2vmin;
        border-radius: 5px;
        border: 1px solid #CECECE;
        background: #FFF;
        box-shadow: 3px 3px 4px 0px rgba(0, 0, 0, 0.08);
            }



        @media screen and (max-width: 800px) {
            .corpo-card{
                width: 100%;
                padding: 20px 15px;
            }
            
            .nome-prestador{
                font-size: 16px;
            }
            .imagem-banner2{
                width: 100%;
            }
            .imagem-banner{
                width: 100%;
            }
        }
        
        
        @media screen and (max-width: 600px) {
            .imagem-banner2{
                width: 100%;
            }
            .imagem-banner{
                width: 100%;
            }
            .corpo-card{
                width: 100%;
                padding: 3.5vmin 3vmin;
            }
            .nome-prestador{
                font-size: 1rem;
            }
        }
</style>