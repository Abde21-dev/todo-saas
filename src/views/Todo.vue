<template>
  <div>
    <NavBar />
  </div>
  <div>
    <AddTodo />
  </div>
  <div>
    <Count />
  </div>
  <div>
    <ListTodo />
  </div>
</template>

<script setup>
import AddTodo from '@/components/AddTodo.vue';
import Count from '@/components/Count.vue';
import ListTodo from '@/components/ListTodo.vue';
import NavBar from '@/components/NavBar.vue';
</script>