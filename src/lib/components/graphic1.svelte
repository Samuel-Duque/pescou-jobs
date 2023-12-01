<script>
    import '../../styles.css';
    import Header from '$lib/components/Header-Prestador-servicos.svelte';
    import Chart from 'chart.js/auto';
    import { onMount } from 'svelte';
    import arrow_right from '$lib/assets/icons/slight-arrow-right.svg'
    import papericon from '$lib/assets/icons/paper-icon.svg'
      // @ts-ignore
      let canvas;
      // @ts-ignore
      let canvas2;
      // @ts-ignore
      const data = {
  labels: ['Seg', 'Ter','Qua','Qui','Sex'],
  datasets: [
    {

      data: [0, 0, 0, ,0, 0],
      borderColor: '#FFF',
      backgroundColor: '#D9D9D9',
    },
    {
      
      data: [9,15,5,18,24],
      borderColor: '#FFF',
      backgroundColor: 'rgba(109, 176, 255, 0.50',
    }
  ]
};
        onMount(() => {
        // @ts-ignore
        if (canvas2 && canvas2.getContext) {
          const ctx = canvas2.getContext('2d');
          if (ctx) {
            new Chart(ctx, {
                type: 'bar',
                data: data,
                options: {
                  
                  responsive: true,
                  maintainAspectRatio: false,
                  // @ts-ignore
                  barThickness: 30,
                    plugins: {
                        legend: {
                            display: false,
                        }
                    },
                    scales: {

                        x: {
                            grid: {
                                display: false,
                            },
                            ticks: {
                              font: {
                                size: 16,
                                family: 'Poppins'
                              },
                        },
                      },
                        y: {
                            grid: {
                                display: true,
                            },
                            ticks: {
                              font: {
                                size: 16,
                                family: 'Poppins'
                              },
                              padding:20,
                            stepSize: 20,
                            maxTicksLimit: 4,
                          }
                        },
                        
                    },                 
                },
                
            });
          }
        }
      });
    </script>
<canvas bind:this={canvas2}/>

<style>
  canvas{
    width:  578px;
    height: 313px;
  }
@media screen and (max-width: 1000px) {
  canvas{
    width:  calc(50%-40px);
    height: 313px;
  }
}
</style>
