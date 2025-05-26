<script lang="js" setup>
import { ref } from 'vue';


const message = ref("Tasks App");
</script>

<template>
  <main>
    <h1>{{ message }}</h1>
    <form>
      <label>
        New Tasks
        <input name="newTask" type="text" placeholder="Enter a new task" />
      </label>
    </form>
  </main>
</template>


<style scoped>

  main {
    max-width: 800px;
    margin: 1rem auto;
   
  }

</style>

