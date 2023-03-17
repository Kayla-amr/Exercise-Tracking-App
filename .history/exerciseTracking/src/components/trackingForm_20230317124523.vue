<template>
    <div id="tracking-form">
        <form>
            <table>
                <tr>
                    <td>Date</td>
                    <td><input type="date" v-model="date"></td>
                </tr>
                <tr>
                    <td>Exercise</td>
                    <td><input type="text" v-model="exercise"></td>
                </tr>
                <tr>
                    <td>Reps</td>
                    <td><input type="number" v-model="reps"></td>
                </tr>
                <tr>
                    <td>Weight</td>
                    <td><input type="number" v-model="weight"></td>
                </tr>
            </table>
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