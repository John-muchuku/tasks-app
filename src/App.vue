<script lang="ts" setup>
import { ref } from 'vue';
import type { Task } from './types';
import TaskForm from './components/TaskForm.vue';

const message = ref("Tasks App");
const tasks = ref<Task[]>([]);

function addTask(newTask: string) {
 tasks.value.push({
   id: crypto.randomUUID(),
   title: newTask,
   done: false
 });
}

</script>

<template>
  <main>

    <h1>{{ message }}</h1>
    <TaskForm @add-task="addTask"/>
    
    <h3>there are {{ tasks.length }} tasks</h3>

  </main>
</template>


<style >

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

