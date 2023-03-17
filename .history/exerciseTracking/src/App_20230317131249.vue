<script setup>
import trackingForm from './components/trackingForm.vue'
import trackingHistory from './components/trackingHistory.vue'
</script>

<template>
    <div id="app">
        <tracking-form />
        <tracking-history />
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
            
              }
            ]
        }
    }
}
</script>