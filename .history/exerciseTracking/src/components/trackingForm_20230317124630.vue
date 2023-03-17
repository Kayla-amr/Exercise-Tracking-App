<template>
    <div id="tracking-form">
        <form>
            <table>
             <thead>
                <tr>
                    <th>Date</th>
                    <th>Exercise</th>
                    <th>Reps</th>
                    <th>Weight</th>
                </tr>
             </thead>
             <tbody>
                
             </tbody>
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