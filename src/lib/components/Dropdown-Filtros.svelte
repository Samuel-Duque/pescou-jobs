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
                    <a href='/' class="head-dropdown"><b>{text}</b></a>
                    <div class="menu">
                        <a href="/ ">{text1}</a> 
                        <a href="/">{text2}</a> 
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
    flex-direction: row;
    padding: 4px 16px;
    gap: 10px;
    align-items: center;
    border: 1px solid var(--theme-color-light-gray);
    background: var(--theme-color-white);
    position: relative;
    border-radius: 8px;
    line-height: 24px;
    min-height: 48px;
    min-width: 50px;
    padding: 12px 16px;


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
    
    color:var(--theme-font-primary);
    text-decoration: none;
    padding-right: 30;
    text-align: justify;
    display: block;
    padding: 10px;

}

.dropdown .menu a{

    border: none;
    padding: 5px;
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

@media screen and (max-width: 1000px) {
    
    .dropdown:hover .menu{
    z-index: 1; 

}
    .dropdown{
        text-wrap: nowrap;
        

    }
    .head-dropdown, .dropdown .menu a {
        font-size: 20px;
    }
}

@media screen and (max-width: 600px) {
    .dropdown:hover .menu{
    z-index: 1; 

}
    .dropdown{
        text-wrap: nowrap;
        margin: auto;
        
    }
    .head-dropdown, .dropdown .menu a {
        font-size: 20px;
    }
}
</style>