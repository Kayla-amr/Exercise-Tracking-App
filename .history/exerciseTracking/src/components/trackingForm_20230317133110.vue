<template>
    <div id="tracking-form">
        <form @submit.prevent="handleSubmit">
            <label for="date">Completed On</label>
            <input type="date" v-model="date">
            
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