<template>
  <div class="wrapper">
    <p>Logo</p>
    <button @click="router.push('/')">Se déconnecter</button>
  </div>
</template>
 
<script setup>
import { useRouter } from 'vue-router'
const router = useRouter()
</script>

<style scoped>
.wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  border-bottom: 1px solid gray;
  height: 32px;
  background-color: rgb(196, 192, 192);
}
p {
  margin-left: 32px;
}
button {
  margin-right: 32px;
  background-color: black;
  color: white;
  border-radius: 5px;
  border: none;
  padding: 3px;
  cursor: pointer;
}
</style>