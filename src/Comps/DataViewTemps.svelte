<script>
  import { onMount } from "svelte";

  let name = "Data";

  let canvas;

  onMount(() => {
    var myChart = new Chart(canvas, {
      type: "line",
      data: {
        labels: [
          "1881",
          "1882",
          "1883",
          "1884",
          "1885",
          "1886",
          "1887",
          "1888",
          "1889",
          "1890",
          "1891",
          "1892",
          "1893",
          "1894",
          "1895",
          "1896",
          "1897",
          "1898",
          "1899",
          "1900",
          "1901",
          "1902",
          "1903",
          "1904",
          "1905",
          "1906",
          "1907",
          "1908",
          "1909",
          "1910",
          "1911",
          "1912",
          "1913",
          "1914",
          "1915",
          "1916",
          "1917",
          "1918",
          "1919",
          "1920",
          "1921",
          "1922",
          "1923",
          "1924",
          "1925",
          "1926",
          "1927",
          "1928",
          "1929",
          "1930",
          "1931",
          "1932",
          "1933",
          "1934",
          "1935",
          "1936",
          "1937",
          "1938",
          "1939",
          "1940",
          "1941",
          "1942",
          "1943",
          "1944",
          "1945",
          "1946",
          "1947",
          "1948",
          "1949",
          "1950",
          "1951",
          "1952",
          "1953",
          "1954",
          "1955",
          "1956",
          "1957",
          "1958",
          "1959",
          "1960",
          "1961",
          "1962",
          "1963",
          "1964",
          "1965",
          "1966",
          "1967",
          "1968",
          "1969",
          "1970",
          "1971",
          "1972",
          "1973",
          "1974",
          "1975",
          "1976",
          "1977",
          "1978",
          "1979",
          "1980",
          "1981",
          "1982",
          "1983",
          "1984",
          "1985",
          "1986",
          "1987",
          "1988",
          "1989",
          "1990",
          "1991",
          "1992",
          "1993",
          "1994",
          "1995",
          "1996",
          "1997",
          "1998",
          "1999",
          "2000",
          "2001",
          "2002",
          "2003",
          "2004",
          "2005",
          "2006",
          "2007",
          "2008",
          "2009",
          "2010",
          "2011",
          "2012",
          "2013",
          "2014",
          "2015",
          "2016",
          "2017",
          "2018",
          "2019",
          "2020",
        ],
        datasets: [
          {
            label: "Temperature over time",
            fill: false,
            data: [
              -0.09, -0.11, -0.18, -0.19, -0.3, -0.22, -0.3, -0.25,
              -0.03, -0.26, -0.35, -0.24, -0.4, -0.29, -0.32, -0.19,
              -0.06, -0.21, -0.23, -0.11, -0.06, -0.2, -0.29, -0.49,
              -0.4, -0.19, -0.31, -0.4, -0.48, -0.39, -0.48, -0.31,
              -0.41, -0.2, -0.12, -0.17, -0.46, -0.33, -0.22, -0.26,
              -0.23, -0.18, -0.28, -0.19, -0.29, -0.06, -0.17, -0.15,
              -0.27, -0.25, -0.07, -0.05, -0.21, -0.23, -0.09, -0.18,
              -0.07, 0.04, -0.07, 0.1, 0.23, 0.23, 0.06, 0.21, 0.22,
              0.16, -0.07, -0.04, -0.04, -0.13, -0.15, 0.1, 0.09,
              0.01, -0.1, -0.17, -0.1, 0.15, 0.11, 0.03, 0.12, 0.08,
              0.09, 0.05, -0.15, -0.03, 0.0, -0.02, 0.03, 0.13, -0.03,
              -0.05, 0.19, 0.02, 0.02, -0.06, 0.08, 0.17, 0.12, 0.31,
              0.31, 0.23, 0.29, 0.29, 0.14, 0.21, 0.26, 0.44, 0.31,
              0.39, 0.42, 0.37, 0.23, 0.26, 0.44, 0.39, 0.36, 0.64,
              0.56, 0.44, 0.44, 0.63, 0.59, 0.64, 0.6, 0.64, 0.69,
              0.52, 0.59, 0.74, 0.61, 0.59, 0.67, 0.7, 0.81, 1.05,
              0.92, 0.84, 0.88, 1.01,
            ],
            cubicInterpolationMode: "monotone",
            backgroundColor: ["rgba(255, 99, 132, 0.2)"],
            borderColor: ["rgba(255, 99, 132, 1)"],
            borderWidth: 1,
          },
        ],
      },
      options: {
        scales: {
          y: {
            beginAtZero: true,
          },
        },
        responsive: true,
        maintainAspectRatio: false,
      },
    });
  });

  //var ctx = document.getElementById('myChart').getContext('2d');
</script>

<article>
  <div class="h1">The Planet is getting Warmer</div>
  <div id="dataScroll">
    <div id="data">
      <canvas bind:this={canvas} />
    </div>
  </div>
</article>

<style>
  article {
    text-align: center;
    padding: 0px 1em 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  .h1 {
    color: #4472c4;
    text-transform: uppercase;
    font-size: 2em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    article {
      max-width: none;
    }

    .h1 {
      font-size: 4em;
    }
  }

  @media (max-width: 640px) {
    article {
      width: 100%;
      padding: 0;
      margin: 0;
      max-width: unset;
    }
  }

  #dataScroll {
    overflow-x: scroll;
  }
  #data {
    width: 120vw;
    margin: auto;
  }
</style>
