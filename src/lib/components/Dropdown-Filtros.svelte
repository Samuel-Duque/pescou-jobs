<title>Listagem de Profissionais</title>
<script lang="ts">
    import downarrow from '$lib/assets/icons/downarrow.svg'
    export let text: string = "";
    export let text1: string = "";
    export let text2: string = "";

    
    
</script>
<div>
    <nav >
        <div class="dropdown-filtro">
            <ul >
                <li class="dropdown">
                    <a href='/profissionais' class="head-dropdown"><b><span class="head">{text}</span></b></a>
                    <div class="menu">
                        <a href="/profissionais">{text1}</a> 
                        <a href="/profissionais">{text2}</a> 
                    </div>
                    <img src={downarrow} alt="">
                </li>
            </ul>
        </div>
    </nav>
</div>

<style>

   .dropdown{
    display: flex;
    width: fit-content;
    height: fit-content;
    border: 1px solid var(--theme-color-light-gray);
    position: relative;
    border-radius: 8px;
    line-height: 24px;
    padding:12px;
    gap: 10px;

}

.dropdown:hover .menu{
    display: inline-block;
    border-radius: 8px;
    margin-top: -0px;
    min-height: 48px;
    min-width: 50px;
    padding: 10px;
    
}

.head-dropdown{
    white-space: nowrap;
    color:var(--theme-font-primary);
    text-decoration: none;
    text-align: justify;
    display: block;
}

.dropdown .menu a{

    border: none;
    padding-bottom: 8px;
    padding-top: 8px;
    text-align: justify;
    border-bottom: 1px solid var(--theme-color-white);
    color:var(--theme-font-primary);
    display: block;
    text-decoration: none;
    transition: border-bottom 0.3s ease-in;

}
.dropdown .menu a:hover{
    border-bottom: 1px solid var(--theme-color-secondary);
}

.menu{
    border: 1px solid var(--theme-color-light-gray);
    background: var(--theme-color-white);
    display: none;
    position: absolute; 
    top: 100%; 
    left: 0; 
    width: 100%;
    text-decoration: none;
    
}
@media screen and (max-width:1300px){
    .dropdown{
        display: flex;
        justify-content: space-between;
        width: 100%;
    }
    .dropdown:hover .menu{
    z-index: 1; 
}

}
@media screen and (max-width:600px){
    .dropdown{
        display: flex;
        justify-content: space-between;
        width: 225px;
    }
    .dropdown:hover .menu{
    z-index: 1; 
}

}

</style>