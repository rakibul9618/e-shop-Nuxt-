<template>
  <div class="max-w-[400px] mx-auto">
    <h1 class="text-center text-4xl font-medium py-10">Todo List</h1>
    <div class="cls">
      <h3 v-for="item of itemLists" :key="item">{{ item.title }}</h3>
      <!-- <h3>{{ itemLists }}</h3> -->
    </div>
  </div>
</template>

<script setup>
const itemLists = useState('itemLists', () => [
  { id: 1, title: 'First Todo' },
  { id: 2, title: 'Second Todo' },
]);
</script>
