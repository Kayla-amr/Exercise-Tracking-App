<template>
    <div id="tracking-form">
        <h2></h2>
        <form @submit.prevent="handleSubmit">
            <div class="date">
                <label for="date">Completed On</label>
                <input type="date" v-model="exercises.date" />
            </div>
            <table>
                <thead>
                    <tr>
                        <th>Sets</th>
                        <th>Reps</th>
                        <th>Weight</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td><input type="text" v-model="exercises.sets" /></td>
                        <td><input type="number" v-model="exercises.reps" /></td>
                        <td><input type="number" v-model="exercises.weight" /></td>
                    </tr>
                </tbody>
            </table>
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
    },
    methods: {
        handleSubmit() {
            const exercise = {
                date: this.exercises.date,
                sets: this.exercises.sets,
                reps: this.exercises.reps,
                weight: this.exercises.weight
            };
            this.$emit('add:exercise', exercise);
        }
    }
}
</script>
  

<style>
.date{
    display: flex;
    flex-direction: column;
    width: 150px;
}
form{
    display: flex;
    flex-direction: column;
}

form button{
    width: 100px;
    padding: 5px;
    margin: 10px 0 0 10px;
    align-self: flex-end;
}
</style>