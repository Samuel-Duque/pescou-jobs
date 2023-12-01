<script>
    import '../../styles.css';
    import Card from '$lib/components/Card.svelte'
    import HeaderSearcher from '$lib/components/Header-Searcher.svelte';
    import arrow_right from '$lib/assets/icons/slight-arrow-right.svg'
    import DropdownFiltros from '$lib/components/Dropdown-Filtros.svelte';
    import ServiceCategories from '$lib/components/ServiceCategories.svelte';
    import SwitchButton from '$lib/components/SwitchButton.svelte';

    const cards = [
    { id: 1, title: 'Card 1' },
    { id: 2, title: 'Card 2' },
    { id: 3, title: 'Card 3' },
    { id: 4, title: 'Card 4' },
    { id: 5, title: 'Card 5' },
    { id: 6, title: 'Card 6' },
    { id: 7, title: 'Card 7' },
    { id: 8, title: 'Card 8' },
    { id: 9, title: 'Card 9' },
    { id: 10, title: 'Card 10' },
    { id: 11, title: 'Card 11' },
    { id: 12, title: 'Card 12' },
  ];
    
</script>

<HeaderSearcher></HeaderSearcher>
<ServiceCategories/>


<div class="corpo-descricao">
    <div class="navbar">
        <span class="inicio">Início</span>
        <img src={arrow_right} alt="Seta p/ direita">
        <span>Pescando um eletricista em Imbiribeira, Recife - PE</span>
    </div>
    <div class="profissional-procurado">
        <span class="header-profissional">Eletricista</span>
        <span class="texto-profissional">Encontre eletricistas qualificados e confiáveis para resolver seus problemas elétricos. Profissionais prontos para atender às suas necessidades de instalação, reparo e manutenção elétrica.</span>
    </div>
    <div class="bottom-navbar">
        
        <div class="filtros-profissionais">
            <DropdownFiltros text="Tempo de experiência" text1="< 2 Anos" text2="> 5 Anos"/>
            <DropdownFiltros text="Faixa de preço" text1="R$ 200" text2="R$ 1.000"/>
            <DropdownFiltros text="Classifição" text1="> 4.5 Estrelas" text2="< 4 Estrelas"/>
            <DropdownFiltros text="Distância" text1="Imbiribeira" text2="Londres"/>
        </div>
        <div class="certificado">
            <div class="certificado-body">
            <SwitchButton/>
            <span class="frase-certificado"><b>Turbo+</b></span>
            </div>
            <div class="certificado-body">
                <SwitchButton/>
                <span class="frase-certificado">Certificado PescouJobs</span>
            </div>    
        </div>
    </div>
</div>

<div class="bloco-inferior">
    <span class="profissionais-achados">20 Eletricistas encontrados em Imbiribeira, Recife, PE</span>
    
    <div class="lista-de-cards">
        {#each cards as card (card.id)}
        <div class="card">
            <a href="/perfil_prestador" style="text-decoration: none; color: var(--theme-text-color-primary) ;"><Card  /></a>
        </div>
        {/each}
    </div>
</div>

<style>
    .frase-certificado{
        /* text-align: center; */
        width: 50%;
    }
    .certificado-body{
        display: flex;
        align-items: center;
        width: 100%;
        gap: 1vmin;
        border: 1px solid aqua
    }
    .card:hover{
        border: 2px solid var(--theme-text-color-secondary);
        border-radius: 6px;
        transform: scale(1.02);
        /* transition: 0.3s; */
    }
    .certificado{
        display: flex;
        align-items: center;
        gap: 1vmin;
    }
    .bottom-navbar{
        display: flex;
        width: 100%;
        justify-content: space-between;
        align-items: center;
    }
    .profissionais-achados{
        font-size: 1.5rem;
        font-weight: 500;
        color: var(--theme-color-dark-gray);
        padding: 3vmin  0px  3vmin 134px ;
    }
    .filtros-profissionais{
        display: flex;
        align-items: center;
        gap: 1vmin;
        }
    .texto-profissional{
        color: var(--theme-color-dark-gray);
        font-size: 20px;
        font-weight: 400;

    }
    .header-profissional{
        color: var(--theme-text-color-primary);
        font-size: 3rem;
        font-weight: 600;

    }
    .profissional-procurado{
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        gap: 5px;
        align-self: stretch;
    }
     
    .inicio{
        color: var(--theme-text-color-secondary) ;
    }
    .navbar{
        display: flex;
        padding: 16px 0px;
        align-items: center;
        gap: 15px;
    }
    .corpo-descricao{
        display: flex;
        width: auto;
        padding: 0px 12vmin;
        flex-direction: column;
        align-items: flex-start;
        gap:23px;
        padding-top: 23px;
        padding-bottom: 23px;
        border-bottom: 1px solid var(--theme-color-light-gray);
    }

    .bloco-inferior{
        display: flex;
        flex-direction: column;
        justify-content: center;
        width: 100%;
    }
    .card{
        /* display: block; */

        transition: transform 0.3s, border 0.3s;
    }
    .lista-de-cards{
        display: grid;
        grid-template-columns: repeat(4,1fr);
        grid-row-gap: 4vmin;
        grid-column-gap: 2.5vmin;
        padding: 0 12vmin;
        width: 100%;

    }

@media screen and (max-width: 1300px) {
    .card:hover{
        border: 0px;

    }
    .certificado-body{
        width: fit-content;
    }
    .bottom-navbar{
        display: grid;
        gap: 1vmin;
    }
    .certificado{
        display: grid;
        grid-template-columns: repeat(1, 1fr);
        gap: 1vmin;
    }
    .filtros-profissionais{
        display: grid;        
        grid-template-columns: repeat(2, 1fr);
        

    }
    
    .profissionais-achados{
        font-size: 1.5rem;
        padding: 30px;
        padding-bottom: 15px;
        justify-content: center;
    }
    .lista-de-cards{
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        /* align-items: center; */
        /* justify-items: center; */
        padding: 1vmin 4vmin;
    }

    .header-profissional{
        font-size: 52px;
    }
    .texto-profissional{
        font-size: 18px;
    }
    .filtros-profissionais{
        padding-left: 0px;
        padding-right: 50px;
    }
}
@media screen and (max-width: 600px) {
    .bottom-navbar{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 0px;
    }
    .filtros-profissionais{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 20px;
        /* border: 1px solid aqua; */

    }
    .lista-de-cards{
        grid-template-columns: repeat(1, 1fr);
        padding: 0 4vmin;
    }
    .corpo-descricao, .bloco-inferior{
        padding: 0 10px;
    }
    .lista-de-cards{
        flex-direction: column;
        align-items: center;
    }
    .header-profissional{
        font-size: 10px;
    }
    .texto-profissional{
        font-size: 16px;
    }
    
}
</style>