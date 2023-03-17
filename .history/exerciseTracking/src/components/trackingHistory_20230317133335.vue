<template>
    <div id="tracking-history">
        <table>
            <thead>
                <tr>
                    <th>Date Completed</th>
                    <th>Exercises</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="exercise in exercises" :key="exercise.id">
                    <td>{{ exercise.date }}</td>
                    <td>{{ exercise.sets }}</td>
                    <td>{{ exercise.reps }}</td>
                    
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