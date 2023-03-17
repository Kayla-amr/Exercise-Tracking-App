<template>
    <div id="tracking-history">
        <table>
            <thead>
                <tr>
                    <th>Date Completed</th>
                    <th>Sets</th>
                    <th>Reps</th>
                    <th>Weight</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="exercise in exercises" :key="exercise.id">
                    <td>{{ exercise.date }}</td>
                    <td>{{ exercise.sets }}</td>
                    <td>{{ exercise.reps }}</td>
                    <td>{{ exercise.weight }}</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script>
export default{
    name: 'tracking-history',
    props: {
        exercises: {
            type: Array
        }
    }
}
</script>

<style>

thead{
    border: 2px solid black;
}

th, td {
    padding: 0 20px;
}
</style>