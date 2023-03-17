<template>
    <div id="tracking-form">
        <form @submit.prevent="handleSubmit">
            <label for="date">Completed On</label>
            <input type="date" v-model="date">
           <input type="select" v-model="exercise">
            <label for="sets">Sets</label>
            <label for="reps">Reps</label>
            <label for="weight">Weight</label>
            <button type="submit">Save</button>
        </form>
    </div>
</template>


<script>
export default {
    name: 'tracking-form',
    data() {
        return {
            exercise: {
                date: '',
                sets: '',
                reps: '',
                weight: ''
            }
        }
    }
}
</script>