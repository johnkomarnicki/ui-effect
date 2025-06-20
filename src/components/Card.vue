<script setup lang="ts">
defineProps<{
  tile: {
    label: string;
    description: string;
  };
}>();
</script>

<template>
  <div tabindex="0" class="card">
    <div class="label-container">
      <p>{{ tile.label }}</p>
      <img src="../assets/material-symbols--north-east.svg" alt="" />
    </div>
    <span>{{ tile.description }}</span>
  </div>
</template>

<style scoped>
.card {
  padding: 12px;
  background-color: rgba(65, 70, 81, 0.64);
  display: flex;
  flex-direction: column;
  min-height: 170px;
  min-width: 208px;
  max-width: 208px;
  border-radius: 8px;
  cursor: pointer;
  /* transition: 300ms ease; */
}

/* .card:hover,
.card:focus {
  transform: translateY(-10px);
} */

.label-container {
  display: flex;
  align-items: self-start;
}

.label-container img {
  margin-left: auto;
  width: 20px;
}

p {
  font-size: 18px;
}

span {
  margin-top: auto;
  font-size: 12px;
}
</style>
