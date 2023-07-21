<script setup>
import Input from '../components/Input.vue';
const inputValue = useState('inputValue', '');
const itemLists = useState('itemLists', () => [
  { id: 1, title: 'First Todo' },
  { id: 2, title: 'Second Todo' },
]);

function greet(event) {
  alert(`First Todo'`);
  // `event` is the native DOM event
  if (event) {
    alert(event.target.tagName);
  }
}

console.log({ inputValue });
</script>

<template>
  <div class="max-w-[400px] mx-auto">
    <h1 class="py-10 text-4xl font-medium text-center">Todo List</h1>
    <p>{{ inputValue }}</p>
    <Input v-model="inputValue" class="text-black" />
    <div class="mt-6">
      <h3
        v-for="item of itemLists"
        :key="item"
        class="bg-[#423a6f] py-3 px-5 border border-purple-800 flex items-center justify-between"
      >
        {{ item.title }}
        <font-awesome-icon
          icon="fa-solid fa-trash"
          @click="greet"
          class="cursor-pointer"
        />
      </h3>
    </div>
  </div>
</template>
