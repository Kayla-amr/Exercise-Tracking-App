<template>
    <div id="tracking-form">
        <form>
            <label for="date">Day Completed</label>
            <input type="date" id="date" name="date" v-model="date">

            <label for="exercise">Exercise</label>
            <input type="text" id="exercise" name="exercise" v-model="exercise">

            <label for="reps">Reps</label>
            <input type="number" id="reps" name="reps" v-model="reps" placeholder="How many reps complete">

            <label for="weight">Weight</label>
            <input type="number" id="weight" name="weight" v-model="weight">

            <label for="date">Date</label>
            <input type="date" id="date" name="date" v-model="date">

            <button>Save</button>
        </form>
    </div>
</template>

<script>
export default {
    name: 'TrackingForm',
    data() {
        return {
            date: '',
            exercise: '',
            reps: '',
            weight: ''
        }
    }
}
</script>