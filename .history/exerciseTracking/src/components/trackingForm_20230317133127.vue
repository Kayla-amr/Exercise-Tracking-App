<template>
    <div id="tracking-form">
        <form @submit.prevent="handleSubmit">
            <label for="date">Completed On</label>
            <input type="date" v-model="date">
            <label for="sets">Sets</label>
            <input type="number" v-model="sets">
            <label for="reps">Reps</label>
            <input type="number" v-model="reps">
            <label for="weight">Weight</label>
            <input type="number" v-model="weight">
            
            <button type="submit">Save</button>
        </form>
    </div>
</template>


<script>
export default {
    name: 'tracking-form',
    data() {
        return {
            exercises: {
                date: '',
                sets: '',
                reps: '',
                weight: ''
            }
        }
    }
}
</script>