<template>
    <div class="container-fluid mt-3">
        <div class="row">
            <div class="col-md-3 col-sm-3">
                <div class="card">
                    <div class="card-body">
                        <h4 class="card-title">John Doe</h4>
                    </div>
                    <div class="card-footer">
                        Test
                    </div>
                </div>
            </div>
            <div class="col-md-3 col-sm-3">
                <div class="card">
                    <div class="card-body">
                        <h4 class="card-title">John Doe</h4>
                    </div>
                    <div class="card-footer">
                        Test
                    </div>
                </div>
            </div>
            <div class="col-md-3 col-sm-3">
                <div class="card">
                    <div class="card-body">
                        <h4 class="card-title">John Doe</h4>
                    </div>
                    <div class="card-footer">
                        Test
                    </div>
                </div>
            </div>
            <div class="col-md-3 col-sm-3">
                <div class="card">
                    <div class="card-body">
                        <h4 class="card-title">John Doe</h4>
                    </div>
                    <div class="card-footer">
                        Test
                    </div>
                </div>
            </div>
        </div>
        <div class="row mt-4">
            <h2 class="text-primary fw-bold text-center">
                Analytics
            </h2>
        </div>
        <div class="row">
            <div class="col-md-6">
                <Bar id="my-chart-id" :options="chartOptions" :data="chartData" />
            </div>
            <div class="col-md-6  d-flex align-items-center justify-content-center">
                <Pie id="my-chart-id" class="chart2" :data="chartData" :options="chartOptions" />
            </div>
        </div>
    </div>
</template>
  
<script>
import { Bar, Pie } from 'vue-chartjs'
import { Chart as ChartJS, Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale } from 'chart.js'
import {ArcElement} from 'chart.js'

ChartJS.register(Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale, ArcElement)

export default {
  name: 'HomePage',
  components: { Bar, Pie },
  data() {
    return {
      chartData: {
        labels: [ 'Jan', 'Feb', 'Mar','Apr','May','June','July','Aug','Sept','Oct','Nov','Dec'],
        datasets: [ { data: [40,20,12,35,23,56,10,23,19,62,11,39],
            label: 'Demo Data',
            backgroundColor: ['#00FFFF', '#ADD8E6', '#00FF00', '#7FFFD4', '#FFA500', '#C0C0C0','#00FFFF', '#ADD8E6', '#00FF00', '#7FFFD4', '#FFA500', '#C0C0C0' ]
         } ],
      },
      chartOptions: {
        responsive: true
      }
    }
  }
}
</script>

<style scoped>
.row .col-md-3 {
    padding: 0px 20px;
}

.container-fluid.mt-3 {
    min-height: calc(100vh - 72px);
}
.chart2{
    height: 370px !important;
    width: 370px !important;
}
</style>
  