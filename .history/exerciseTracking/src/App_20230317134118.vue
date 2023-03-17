<script setup>
import trackingForm from './components/trackingForm.vue'
import trackingHistory from './components/trackingHistory.vue'
</script>

<template>
    <div id="app">
        <tracking-form />
        <tracking-history :exercises="exercises" />

    </div>
</template>

<script>
export default{
    name: 'app',
    components: {
        trackingForm,
        trackingHistory
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
        },
        methods:{
          add-exercise
        }
    }
}
</script>