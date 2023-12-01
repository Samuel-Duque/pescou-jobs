<script>
    import '../../styles.css';
    import lupa from '$lib/assets/icons/lupa.svg';
</script>

<!-- <div class="search">
    <div class="placehold">
        <img src={lupa} alt="">
        <span class="text-hold"></span>
    </div>
</div> -->


<div class="caixa-formulario">
    <form action="" class="formu">
        <div class="icon-and-label">
            <img src={lupa} alt="icone" class="icone">
        </div>
        <div class="input-container">
            <input name="servico" placeholder="Eletricista" type="text" />
        </div>
    </form>
</div>
<style>
    input{
        width: 25vmin;
        background-color: var(--theme-color-white);
        border: none;
        outline: none;
        align-items: center;
        height: 50px;

    }
    .icon-and-label{
        margin-top: 3px;
    }
    .input-container{
        width: 25vmin;
        align-self: stretch;
        color: var(--theme-text-color-secondary);
        outline: none;
        border: none;
    }
    .formu{
        display: flex;
        align-items: center;
        gap: 8px;
    }
    .caixa-formulario{
        display: flex;
        width: 345px;
        padding: 4px 24px;
        border: 1px solid var(--theme-color-light-gray);
        background: var(--theme-color-white);
    }
    @media screen and (max-width:1070px){
        .caixa-formulario{
            visibility: hidden;
        }
        input{
            width: 20vmin;
        }   
    }
</style>