<template>
  <div id="tracking-history">
    <h2>History</h2>
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
export default {
  name: 'tracking-history',
  props: {
    exercises: {
      type: Array
    }
  },
  methods:{
    sortDate(){
      this.exercises.sort((a, b) => {
        return new Date(b.date) - new Date(a.date);
      });
    }
  }
}
</script>

<style>
th,
td {
  padding: 0 20px;
}
</style>
