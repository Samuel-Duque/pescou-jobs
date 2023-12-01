<script lang="ts">
  import '../../styles.css'
</script>
<body>
    <main class="card" >
        <section class="card__header">
          <h3>Domingo 19</h3>
          <h3>Novembro 2023</h3>
        </section>
        <section class="card__body">
          <ul class="card__body--days">
            <li>Seg</li>
            <li>Ter</li>
            <li>Qua</li>
            <li>Qui</li>
            <li>Sex</li>
            <li>Sab</li>
            <li>Dom</li>
          </ul>
          <ul class="card__body--dates">
            <li class="prev">30</li>
            <li class="prev">31</li>
            <li>1</li>
            <li>2</li>
            <li>3</li>
            <li>4</li>
            <li>5</li>
            <li>6</li>
            <li>7</li>
            <li>8</li>
            <li>9</li>
            <li>10</li>
            <li>11</li>
            <li>12</li>
            <li>13</li>
            <li>14</li>
            <li>15</li>
            <li>16 </li>
            <li>17</li>
            <li>18</li>
            <li class="dia-hoje">19</li>
            <li>20</li>
            <li>21</li>
            <li>22</li>
            <li>23</li>
            <li>24</li>
            <li>25</li>
            <li>26</li>
            <li>27</li>
            <li>28</li>
            <li>29</li>
            <li>30</li>
            <li>31</li>
            <li class="next">1</li>
            <li class="next">2</li>
          </ul>
        </section>

      </main>
</body>
<!-- {/if} -->

<style >

  :root{
    --theme-color-primary: #1e88e5;
    --theme-color--white: #fff;
  }
  .card__body--dates li:hover{
    border-radius: 50px;
    background: #ccc;
    cursor: pointer;
  }
  .dia-hoje {
    background: var(--theme-color-primary);
    color: var(--theme-color--white);
    border-radius: 50px;
      }
  .card__body--dates li.prev:hover,.card__body--dates li.next:hover{
    background: #161616;
    cursor: pointer;

  }
  .card__body--dates li.prev,.card__body--dates li.next{
    color: #ccc;
  }
  .card__body--dates li{
    height: 31px;
    width: 31px;
    /* text-align: center; */
    display: grid;
    grid-template-columns: auto auto;
    place-items: center;
    font-weight: bold;
    position: relative;
    justify-content: center;
    align-items: center;
    padding: 3px;
    margin-left:10px;
  }
  .card__body--dates{
    display: grid;
    grid-template-columns: repeat(7, 1fr);
    grid-template-rows: repeat(5, 1fr);
    grid-gap: 1px;
    list-style: none;
  }
  .card__body--days{
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 4vmin;
  }
  .card__body{
    padding: 1.5vmin 2vmin;
    border-top: 1px solid #ccc;
    border-bottom: 1px solid #ccc;
  }
  li{
    flex: 1;
    font-weight: bold;
    text-transform: uppercase;
    text-align: center;
    color: gray;
    margin: 0 1px;
  }
  .card__header{
    padding: 2vmin 2.25vmin;
    color: gray;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .card{
    background: white;
    width: 400px;
    border-radius: 10px;
    margin: auto auto;
    display: grid;
    box-shadow: 3px 3px 4px 0px rgba(0, 0, 0, 0.082),-1px -1px 4px 1px rgba(0, 0, 0, 0.082);

  }
  
  ul{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    list-style: none;

  }
  @media (max-width: 600px) {
    .card{
      width: 100%;
    }
  }
</style>
