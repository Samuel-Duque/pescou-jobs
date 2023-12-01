<script>
    import '../../styles.css'
</script>



<style>
    body{
        border: 0;
        margin-inline-start: 0;
        margin-inline-end: 0;
    }
    
    ul{
        display: flex;
        width: auto;
        padding: 20px 132px;
        justify-content: space-between;
        align-items: center;
        border-bottom: 1px solid var(--theme-color-light-gray);
        background: var(--theme-text-color-tertiary);
        flex-wrap: wrap; 
        
    }
    
    li{
        display: inline;   
        transition: border-bottom 0.3s ease-in;
        border-bottom: 1px solid var(--theme-color-white);
    }


    li:hover{
        border-bottom: 1px solid var(--theme-color-secondary);
    }

    a{
        /* padding: 5px; */
        color: var(--theme-text-color-primary);
        text-decoration: none;
        font-weight: 400;
        font-size: 1.0rem;
    }

    @media screen and (max-width:1000px){

        li{
            padding: 5px;

        }
    }
    @media (max-width: 680px) {
        ul{
            display: grid;
            grid-template-rows: repeat(5,1fr);
            justify-content: center;
            /* align-items: center; */
            text-align: center;
            padding: 0px 60px;
        }
        a {
            font-size: 0.8rem; 
        }
    }
</style>

    

<body>
    <nav>
        <ul>
            <li><a href='/'>Desenvolvimento de Software</a></li>
            <li><a href='/'>Engenheiro civil</a></li>
            <li><a href='/'>Personal Trainer</a></li>
            <li><a href='/'>Desing Gráfico</a></li>
            <li><a href='/'>Caminhoneiro</a></li>
            <li><a href='/'>Videomaker</a></li>
            <li><a href='/'>Encanador</a></li>
            <li><a href='/'>Eletricista</a></li>
            <li><a href='/'>Consultor</a></li>
        </ul>
    </nav>
</body>