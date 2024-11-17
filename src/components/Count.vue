<template>
  <div class="wrapper">
    <div v-if="todos.length === 0">Vous n'avez pas de tâche à faire</div>
    <div v-else class="bottom">
      <p><strong>Effectuée :</strong> {{ trueCount }}</p>
      <p><strong>À faire :</strong> {{ falseCount }}</p>
    </div>
  </div>
</template>
 
<script setup>
import { computed } from 'vue';
import { useStore } from 'vuex';

const store = useStore();
const todos = computed(() => store.state.todos);

const trueCount = computed(() => store.getters.getDoneTrue)
const falseCount = computed(() => store.getters.getDoneFalse)

</script>

<style scoped>
.wrapper {
  display: flex;
  justify-content: center;
  margin-top: 16px;
}
.bottom .home {
  display: flex;
  gap: 32px;
}
</style>