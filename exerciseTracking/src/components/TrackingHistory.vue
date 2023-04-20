<template>
  <div id="tracking-history">
 
 
   
    <div class="benchPressHistory" for="benchPresses" v-if="exerciseOption === 'benchPresses'">
    <h2>History</h2>
    <table>
      <thead>
        <tr>
          <th>Date Completed</th>
          <th>Sets</th>
          <th>Reps</th>
          <th>Weight</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="benchPress in benchPresses" :key="benchPress.id">
          <td>{{ benchPress.date }}</td>
          <td>{{ benchPress.sets }}</td>
          <td>{{ benchPress.reps }}</td>
          <td>{{ benchPress.weight }}</td>
        </tr>
      </tbody>
    </table>
    </div>
 
 
    <div class="runningHistory" for="running" v-if="exerciseOption === 'running'">
    <h2>History</h2>
    <table>
      <thead>
        <tr>
          <th>Date Completed</th>
          <th>Distance</th>
          <th>Time</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="run in running" :key="run.id">
          <td>{{ run.date }}</td>
          <td>{{ run.distance }}</td>
          <td>{{ run.time }}</td>
        </tr>
      </tbody>
    </table>
    </div>
  </div>
 </template>
 
 
 <script>
 import TrackingForm from './TrackingForm.vue'
 
 
 export default {
  name: 'tracking-history',
  props: {
    benchPresses: {
      type: Array
    },
    running: {
      type: Array
    },
    exerciseOption: {
      type: String
    }
  }
 }
 </script>
 
 
 <style>
 th,
 td {
  padding: 0 20px;
 }
 </style>
 
 
 
 
 
 