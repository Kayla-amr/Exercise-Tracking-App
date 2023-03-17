<template>
    <div id="tracking-form">
        <form @submit.prevent="handleSubmit">
            <label for="date">Completed On</label>
            <input type="date" v-model="date">
            <select v-model="selected">
  <option disabled value="">Please select one</option>
    <option>Sets</option>
</select>
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