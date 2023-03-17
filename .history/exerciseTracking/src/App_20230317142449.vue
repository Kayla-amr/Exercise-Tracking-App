<script setup>
import TrackingForm from './components/TrackingForm.vue'
import TrackingHistory from './components/TrackingHistory.vue'
</script>

<template>
  <div id="app">
    <tracking-form @add:exercise="addExercises" />
    <tracking-history :exercises="exercises" />
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
      exercises: [
        {
          id: 1,
          date: '2021-01-01',
          sets: '3',
          reps: '12',
          weight: '50'
        },
        {
          id: 2,
          date: '2021-01-02',
          sets: '3',
          reps: '20',
          weight: '10'
        },
        {
          id: 3,
          date: '2021-01-03',
          sets: '3',
          reps: '15',
          weight: '40'
        }
      ]
    }
  },

  methods: {
    addExercises(exercise) {
      const addId = this.exercises.length > 0 ? this.exercises[this.exercises.length - 1].id : 0

      const id = addId + 1

      const newExercises = {
        id,
        ...exercise
      }

      this.exercises = [...this.exercises, exercise]
    }
  }
}
</script>


<style>

</style>