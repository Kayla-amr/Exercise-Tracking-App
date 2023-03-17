<template>
    <div id="tracking-form">
        <form>
            <label for="exercise">Exercise</label>
            <input type="text" id="exercise" name="exercise" v-model="exercise">

            <label for="reps">Reps</label>
            <input type="number" id="reps" name="reps" v-model="reps">

            <label for="weight">Weight</label>
            <input type="number" id="weight" name="weight" v-model="weight">

            <label for="date">Date</label>
            <input type="date" id="date" name="date" v-model="date">

            <button>
                
            </button>
        </form>
    </div>
</template>