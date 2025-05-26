<script lang="ts" setup>
import { ref } from 'vue';

const emit = defineEmits<{
  addTask: [newTask: string]
}>();


const newTask = ref("");

function formSubmitted () {
emit("addTask", newTask.value.trim());
}

</script>



<template>
     <form @submit.prevent="formSubmitted">
      <label>
        New Tasks
        <input v-model="newTask" name="newTask" type="text" placeholder="Enter a new task" />
      </label>

      <div class="button-container">
           <button>Add</button>
      </div>

    </form>
</template>