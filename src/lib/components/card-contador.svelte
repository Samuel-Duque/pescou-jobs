<script lang="ts">
  import { onMount } from "svelte";
  import "../../styles.css";
  let valuesDisplays;
  let interval = 5000;

  onMount(() => {
    valuesDisplays = document.querySelectorAll(".num");
    console.log(valuesDisplays);

    valuesDisplays.forEach((valuesDisplay) => {
      let startValue = 0;
      let endValue = parseInt(valuesDisplay.getAttribute("data-val") ?? "0");
      console.log(endValue);
      let duration = Math.floor(interval / endValue);

      let counter = setInterval(function () {
        startValue += 1;
        valuesDisplay.textContent = "+ " + startValue.toString();
        if (startValue === endValue) {
          clearInterval(counter);
        }
      }, duration);
    });
  });
</script>

<head>
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css"
  />
</head>

<body>
  <div class="wrapper">
    <div class="container">
      <i class="fa-solid fa-screwdriver-wrench"></i>
      <span class="num" data-val="400">000</span>
      <span class="text">Serviços prestados</span>
    </div>

    <div class="container">
      <i class="fa-solid fa-smile-beam"></i>
      <span class="num" data-val="463">000</span>
      <span class="text">Clientes Felizes</span>
    </div>

    <div class="container">
      <i class="fa-solid fa-list"></i>
      <span class="num" data-val="225">000</span>
      <span class="text">Áreas de serviço</span>
    </div>

    <div class="container">
      <i class="fa-solid fa-star"></i>
      <span class="num" data-val="280">000</span>
      <span class="text">5 Estrelas</span>
    </div>
  </div>
</body>

<style>
  .wrapper {
    /* position: absolute; */
    /* width: 80vw; */
    /* transform: translate(-50%, -50%); */
    /* top: 50%; */
    /* left: 50%; */
    display: flex;
    justify-content: space-around;
    gap: 40px;
  }
  .container {
    background: rgba(255, 255, 255, 0.1); /* fundo semi-transparente */
    backdrop-filter: blur(10px);
    width: 28vmin;
    height: 28vmin;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    padding: 1em 0;
    position: relative;
    font-size: 1rem;
    border-radius: 0.5em;
    border-bottom: 3px solid var(--theme-color-primary);
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  }
  i {
    color: var(--theme-color-primary);
    font-size: 2.5em;
    text-align: center;
  }
  span.num {
    color: var(--theme-color-primary);
    display: grid;
    place-items: center;
    font-weight: 600;
    font-size: 3em;
    margin-left: -20px;
  }
  span.text {
    color: var(--theme-text-color-primary);
    font-size: 1.1rem;
    text-align: center;
    pad: 0.7em 0;
    font-weight: 600;
    line-height: 0;
  }

  @media screen and (max-width: 1200px) {
    .wrapper {
      width: 85vw;
    }
    .container {
      height: 26vmin;
      width: 26vmin;
      font-size: 12px;
    }
  }
  @media screen and (max-width: 900px) {
    .wrapper {
      width: 90vw;
      flex-wrap: wrap;
      gap: 30px;
    }
    .container {
      background-color: var(--theme-color-secondary);
      height: 30vmin;

      width: calc(50% - 40px);
      font-size: 14px;
      color: var(--theme-color-white);
      border-bottom: 5px solid var(--theme-color-primary);
    }
    .container span.num {
      margin-left: -30px;
    }
    .container span.text {
      color: var(--theme-color-white);
      font-weight: 500;
      font-size: 1rem;
    }
  }
  @media screen and (max-width: 480px) {
    .wrapper {
      gap: 15px;
    }
    .container {
      height: 25vmin;
      width: 100%;
      font-size: 8px;
    }
  }
</style>
