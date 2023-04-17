<script setup>
const counter = useState("counter", () => Math.round(Math.random() * 1000));
const color = useColor();
</script>

<template>
  <!-- <div>
    Counter: {{ counter }}
    <button @click="counter++">+</button>
    <button @click="counter--">-</button>
    <br />
    Color: {{ color }}
    <div m-17 text-blue-500>Helloo</div>
    <button m-7 rounded text-teal-400>Button</button>
  </div> -->
  <Suspense>
    <Child />
    <template #fallback>
     Loading....
    </template>
  </Suspense>
</template>
