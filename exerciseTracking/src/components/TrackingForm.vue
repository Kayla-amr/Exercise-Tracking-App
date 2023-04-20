<template>
  <div id="tracking-form">
    <form>
      <div class="form-group">
        <label for="exerciseOption">Select Exercise to Track:</label>
        <select class="form-control" id="exerciseOption" v-model="exerciseOption">
          <option :value="null">Choose...</option>
          <option :value="'benchPresses'">Bench Press</option>
          <option :value="'running'">Running</option>
        </select>
      </div>
    </form>
 
 
    <div class="benchPress" for="benchPress" v-if="exerciseOption === 'benchPresses'">
   
    <h2>Enter Bench Press</h2>
    <form @submit.prevent="handleSubmit">
      <div class="date">
        <label for="date">Completed On</label>
        <input type="date" v-model="benchPresses.date" />
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
            <td><input type="text" v-model="benchPresses.sets" /></td>
            <td><input type="number" v-model="benchPresses.reps" /></td>
            <td><input type="number" v-model="benchPresses.weight" /></td>
          </tr>
        </tbody>
      </table>
      <button type="submit">Save</button>
    </form>
    </div>
 
 
    <div class="running" for="running" v-if="exerciseOption === 'running'">
    <h2>Enter Time</h2>
    <form @submit.prevent="handleRunningSubmit">
      <div class="date">
        <label for="date">Completed On</label>
        <input type="date" v-model="running.date" />
      </div>
      <table>
        <thead>
          <tr>
            <th>Distance</th>
            <th>Time</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td><input type="text" v-model="running.distance" /></td>
            <td><input type="number" v-model="running.time" /></td>
          </tr>
        </tbody>
      </table>
      <button type="submit">Save</button>
    </form>
  </div>
  </div>
 </template>
 
 
 <script>
 export default {
  name: 'tracking-form',
  data() {
    return {
      exerciseOption: null,
      benchPresses: {
        date: '',
        sets: '',
        reps: '',
        weight: ''
      },
      running: {
        date: '',
        distance: '',
        time: ''
      }
    }
  },
  methods: {
    handleSubmit() {
      const benchPress = {
        date: this.benchPresses.date,
        sets: this.benchPresses.sets,
        reps: this.benchPresses.reps,
        weight: this.benchPresses.weight
      }
      this.$emit('add:benchPresses', benchPress)
    },
    handleRunningSubmit() {
      const run = {
        date: this.running.date,
        distance: this.running.distance,
        time: this.running.time
      }
      this.$emit('add:running', run)
    }
  },
  watch: {
  exerciseOption: function (newVal) {
    this.$emit('update:exerciseOption', newVal);
  }
 }
 }
 </script>
 
 
 <style>
 .date {
  display: flex;
  flex-direction: column;
  width: 150px;
 }
 form {
  display: flex;
  flex-direction: column;
 }
 
 
 form button {
  width: 100px;
  padding: 5px;
  margin: 10px 0 0 10px;
  align-self: flex-end;
 }
 </style>
 
 
 
 
 
 
 