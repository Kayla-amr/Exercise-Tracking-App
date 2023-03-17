<template>
    <div id="tracking-form">
        <form>
            <label for="date">Date</label>
            <input type="date" v-model="date">
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
                    <td><input type="text" v-model="sets"></td>
                    <td><input type="number" v-model="reps"></td>
                    <td><input type="number" v-model="weight"></td>
                </tr>
             </tbody>
            </table>
        </form>
    </div>
</template>

<script>

</script>