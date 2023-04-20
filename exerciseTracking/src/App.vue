<script setup>
import TrackingForm from './components/TrackingForm.vue'
import TrackingHistory from './components/TrackingHistory.vue'
</script>

<template>
  <div id="app">
    <tracking-form @add:benchPresses="addBenchPresses" @add:running="addRunning" @update:exerciseOption="exerciseOption=$event"/>
    <tracking-history :benchPresses="benchPresses" :running="running" :exerciseOption="exerciseOption"/>
  </div>
</template>

<script>
export default {
  name: 'app',
  components: {
    TrackingForm,
    TrackingHistory
  },
  data() {
    return {
      exerciseOption: null,
      benchPresses: [
        {
          id: 1,
          date: '2023-01-01',
          sets: '3',
          reps: '12',
          weight: '50'
        },
        {
          id: 2,
          date: '2022-02-01',
          sets: '3',
          reps: '20',
          weight: '10'
        },
        {
          id: 3,
          date: '2021-03-01',
          sets: '3',
          reps: '15',
          weight: '20'
        }
      ],
      running:[
        {
          id: 1,
          date: '2023-01-01',
          distance: '3',
          time: '12',
          weight: '50'
        },
        {
          id: 2,
          date: '2022-02-01',
          distance: '3',
          time: '20'
        },
        {
          id: 3,
          date: '2021-03-01',
          distance: '3',
          time: '15'
        }
      ]
    }
  },

  methods: {
    addBenchPresses(benchPress) {
      const addId = this.benchPresses.length > 0 ? this.benchPresses[this.benchPresses.length - 1].id : 0

      const id = addId + 1

      const newBenchPress = {
        id,
        ...benchPress
      }

      this.benchPresses = [...this.benchPresses, benchPress]
    },
    addRunning(running) {
      const addId = this.running.length > 0 ? this.running[this.running.length - 1].id : 0

      const id = addId + 1

      const newRunning = {
        id,
        ...running
      }

      this.running = [...this.running, running]
    }
    
  }
}
</script>

<style>
#app {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
  background-color: #f5f5f5;
}
</style>
