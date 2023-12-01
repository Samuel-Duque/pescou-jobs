<script>
// @ts-nocheck

import banner from '$lib/assets/foto-servico1.svg'
// @ts-ignore
export let Texto;
export let id;
</script>

<div class="corpo-servico" class:corpo-servico-impar={id % 2 === 1} >
    <div class="container-serv">
        <div class="foto-nome">
            <div class="foto">
                <img src={banner} alt="Foto do prestador de serviço">
            </div>
            <div class="nome">
                <span>Serviço</span>
            </div>
        </div>
        <div class="id-preco-status">
            <span class="id">{id}</span>
            <span class="preco">R$ 60,00</span>
            <!-- svelte-ignore missing-declaration -->
            <div class="status" class:finalizado={Texto === 'Finalizado'} class:nao-finalizado={Texto !== 'Finalizado'}>
                
                {Texto}
            </div>
        </div>
    </div>
</div>

<style>
    .container-serv{
        display: flex;
        width: 100%;
        align-items: center;
        justify-content: space-between;
        gap: 1%;
    }
    .nao-finalizado{
        background-color: #EE443A4D;
        color: #A12626;
    }
    .finalizado{
        background-color:  #8BCDFB4D;
        color: #268ABC;
    }
    .id-preco-status .id{
        width: 1vw;
    }
    .id-preco-status .preco{
        font-size: 1.125rem;
    }
    .id-preco-status .status{
        
        width: 151px;
        border-radius: 5px;
        padding: 10px 10px;
        font-weight: 500;
        text-align: center;
    }

    .id-preco-status{

    display: flex;
    align-items: center;
    width: auto;
    height: auto;
    justify-content: space-between;
    gap: 7.7vw;
    }
    .foto-nome img{
    height: 73px;
    width: 100px;
    border-radius: 5px;
    }
    .foto-nome{
    gap: 1rem;
    display: flex;
    align-items: center;
    }
    .corpo-servico{
    display: flex;
    width: auto;
    height: auto;
    border: 0.2px solid var(--theme-color-light-gray);
    padding: 1.5em 2.5em;
    background: rgba(214, 214, 255, 0.50);
    align-items: center;
    /* justify-content: space-between; */

    }
    .corpo-servico-impar{
    display: flex;
    padding: 1.5rem 2.5rem;
    background: var(--theme-color-white);
    align-items: center;
    justify-content: space-between;
    }


    @media screen and (max-width:43.75rem){
    
    .id-preco-status{
        gap: 0.1em;
    }
    .foto-nome .foto{
        display: none;
        visibility: hidden;
    }
    .id-preco-status .id{
        display: none;
    }
    .foto-nome{
        border: 1px solid green;
        padding: auto;
        gap: 0.5em; 
        margin: auto;
        display: block;
        align-items: center;
        justify-content: center;
    }
}
</style>