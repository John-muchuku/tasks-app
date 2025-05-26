<script lang="js" setup>
import { ref } from 'vue';


const message = ref("Tasks App");
const newTask = ref("");

function formSubmitted () {
  console.log(newTask.value);
}



</script>

<template>
  <main>

    <h1>{{ message }}</h1>

    <form @submit.prevent="formSubmitted">
      <label>
        New Tasks
        <input v-model="newTask" name="newTask" type="text" placeholder="Enter a new task" />
      </label>

      <div class="button-container">
           <button>Add</button>
      </div>

    </form>

    <h3>{{ newTask }}</h3>

  </main>
</template>


<style scoped>

  main {
    max-width: 800px;
    margin: 1rem auto;
   
  }

  .button-container {
    display: flex;
    justify-content: center;
    margin-top: 1rem;
  }

</style>

