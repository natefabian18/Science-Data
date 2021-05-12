<script>
  import { onMount } from 'svelte';

  let name = "Data";

  let canvas;

  onMount(()=>{
    var myChart = new Chart(canvas, {
    type: 'bar',
    data: {
        labels: ['Red', 'Blue', 'Yellow', 'Green', 'Purple', 'Orange'],
        datasets: [{
            label: '# of Votes',
            data: [12, 19, 3, 5, 2, 3],
            backgroundColor: [
                'rgba(255, 99, 132, 0.2)',
                'rgba(54, 162, 235, 0.2)',
                'rgba(255, 206, 86, 0.2)',
                'rgba(75, 192, 192, 0.2)',
                'rgba(153, 102, 255, 0.2)',
                'rgba(255, 159, 64, 0.2)'
            ],
            borderColor: [
                'rgba(255, 99, 132, 1)',
                'rgba(54, 162, 235, 1)',
                'rgba(255, 206, 86, 1)',
                'rgba(75, 192, 192, 1)',
                'rgba(153, 102, 255, 1)',
                'rgba(255, 159, 64, 1)'
            ],
            borderWidth: 1
        }]
    },
    options: {
        scales: {
            y: {
                beginAtZero: true
            }
        },
        responsive: true,
        maintainAspectRatio: true
    }
});
  });

  //var ctx = document.getElementById('myChart').getContext('2d');
  
</script>

<main>
  <div class="h1">{name}!</div>
  <div id="data">
    <canvas bind:this={canvas} ></canvas>
  </div>
</main>

<style>
  main {
    text-align: center;
    padding: 0px 1em 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  .h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }

  #data {
    width: 70vw;
    margin:auto;
  }
</style>
