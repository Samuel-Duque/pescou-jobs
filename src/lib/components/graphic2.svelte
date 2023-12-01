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

      data: [0, 0, 0, 0, 0],
      borderColor: '#FFF',
      backgroundColor: '#D9D9D9',
    },
    {
      
      data: [100,500,320,420,190],
      borderColor: '#FFF',
      backgroundColor: 'rgba(109, 176, 255, 0.50)',
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
                        },
                        tooltip:{
                          callbacks: {
                            label: function(context) {
                              var label = context.dataset.label || '';
                              if (label) {
                                label += ': ';
                              }
                              if (context.parsed.y !== null) {
                                label += 'R$ ' + context.parsed.y.toFixed(2).replace('.', ',');
                              }
                              return label;
                            }
                          }
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
                              padding:20,
                            stepSize: 100,
                            font: {
                                size: 16,
                                family: 'Poppins',
                            },
                            callback: function(value, index, values) {
                                // @ts-ignore
                                return 'R$ ' + value.toFixed(2).replace('.', ',');
                            }
                          }
                        },
                        
                    },                 
                },
                
            });
          }
        }
      });
    </script>
<canvas bind:this={canvas2} width="578px" height="313px"/>
<style>
  canvas{
    width: 578px;
    height: 313px;
    overflow: visible;
  }
</style>

