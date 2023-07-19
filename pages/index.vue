<script setup>
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
</script>

<template>
  <div class="max-w-[400px] mx-auto">
    <h1 class="py-10 text-4xl font-medium text-center">Todo List</h1>
    <div class="cls">
      <h3
        v-for="item of itemLists"
        :key="item"
        class="bg-[#423a6f] py-3 px-5 border border-purple-800 flex items-center justify-between"
      >
        {{ item.title }}
        <font-awesome-icon icon="fa-solid fa-trash" @click="greet" class="cursor-pointer"/>
      </h3>
    </div>
  </div>
</template>
