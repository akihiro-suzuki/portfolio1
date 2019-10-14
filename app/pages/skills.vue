<template>
  <article>
    <div class="parent">
      <h1>As Software Engineer</h1>
      <div class="flex-container">
        <div class="programming">
          <Bar :chartdata="programmingData" :options="programmingOptions" />
        </div>
        <div>
          <Bar :chartdata="dbData" :options="dbOptions" />
        </div>
      </div>
      <h1>As Jazz Drummer</h1>
      <div class="flex-container">
        <div class="programming">
          <Rader :chartdata="drummingData" :options="drummingOptions" />
        </div>
        <div class="programming">
          <Rader :chartdata="favDrummerData" :options="favDrummerOptions" />
        </div>
      </div>
    </div>
  </article>
</template>
<script>
import Chart from 'chart.js'
import Bar from '~/components/Bar'
import Rader from '~/components/Rader'

export default {
  components: {
    Bar,
    Rader
  },
  data: () => {
    return {
      programmingData: {
        labels: ['Java', 'C#', 'JavaScript', 'VB.NET', 'PHP', 'python'],
        datasets: [
          {
            label: 'プログラミング言語歴(年数)',
            backgroundColor: Chart.helpers
              .color('rgb(99, 255, 132)')
              .alpha(0.5)
              .rgbString(),
            data: [5, 3, 2, 0.6, 0.6, 0.2]
          }
        ]
      },
      programmingOptions: {
        responsive: true,
        maintainAspectRatio: false
      },
      dbData: {
        labels: ['Oracle', 'Mysql', 'SQLite', 'MariaDB', 'Postgres'],
        datasets: [
          {
            label: 'DB(年数)',
            backgroundColor: Chart.helpers
              .color('rgb(255, 132, 99)')
              .alpha(0.5)
              .rgbString(),
            data: [4, 2, 2.5, 1, 1]
          }
        ]
      },
      dbOptions: {
        responsive: true,
        maintainAspectRatio: false,
        scales: {
          yAxes: [
            {
              ticks: {
                beginAtZero: true,
                min: 0
              }
            }
          ]
        }
      },
      drummingData: {
        labels: ['Jazz', 'Rock', 'Ballad', 'Latin', 'Pop'],
        datasets: [
          {
            label: '得意スタイル',
            backgroundColor: Chart.helpers
              .color('rgb(132, 99, 255)')
              .alpha(0.5)
              .rgbString(),
            data: [5, 2, 4, 3, 3]
          }
        ]
      },
      drummingOptions: {
        responsive: true,
        maintainAspectRatio: false,
        scale: {
          ticks: {
            label: false,
            min: 0,
            fixedStepSize: 1,
            showLabelBackdrop: false,
            color: '#eee'
          }
        }
      },
      favDrummerData: {
        labels: [
          'PhilyJoeJones',
          'BrianBlade',
          'ElvinJones',
          'MaxRoach',
          'TonyWilliams'
        ],
        datasets: [
          {
            label: '好きなドラマー',
            backgroundColor: Chart.helpers
              .color('rgb(255, 99, 255)')
              .alpha(0.5)
              .rgbString(),
            data: [4, 5, 4, 3, 2]
          }
        ]
      },
      favDrummerOptions: {
        responsive: true,
        maintainAspectRatio: false,
        scale: {
          ticks: {
            label: false,
            min: 0,
            fixedStepSize: 1,
            showLabelBackdrop: false,
            color: '#eee'
          }
        }
      }
    }
  }
}
</script>
<style scoped>
.flex-container {
  display: flex;
  flex-wrap: wrap;
  width: 1000px;
  margin: 0 auto;
  justify-content: space-around;
}
h1 {
  padding: 20px 0px;
  font-family: 'Courier New', Courier, monospace;
  color: darkgray;
}
@media screen and (max-width: 767px) {
  .flex-container {
    width: auto;
  }
}
</style>
