<template>
  <div class="wrapper">
    <h1>Liste de tâche</h1>
    <div>
      <input type="text" placeholder="entrez une nouvelle tâche"
      v-model="newTodo" >
      <button @click="addTodo">Ajouter</button>
    </div>
    
    
    </div>
</template>
 
<script setup>
import {  ref } from 'vue'
import { useStore } from 'vuex'

const store = useStore();
const newTodo = ref();

const addTodo = () => {
  const todo = {
    id: Date.now(),
    title: newTodo.value,
    done: false,
  };
  store.dispatch("addTodo", todo);
  newTodo.value = "";
}

</script>

<style scoped>
input {
  padding: 5px;
  width: 40%;
}
button {
  padding: 5px;
  margin-left: 10px;
  border: none;
  border-radius: 5px;
  background-color: yellowgreen;
  color: black;
  cursor: pointer;
}
button:hover {
  background-color: green;
  color: white;
}
</style>