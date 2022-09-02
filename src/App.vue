<template>
  <div>
    <grid-component :myGrid="gridData"></grid-component>
  </div>
</template>

<script setup>
import { ref, onMounted } from "vue";
import GridComponent from "./components/GridComponent.vue";

const gridColumn = ref([
  "fileName",
  "firstName",
  "Surname",
  "propertyDate",
  "propertySelect",
  "propertyDropdown",
]);
const gridData = ref([
  {
    fileName: "audio1",
    firstName: "mike",
    Surname: "peterson",
    propertyDate: "10-22-1967",
    propertySelect: "C",
    propertyDropdown: 2,
  },
  {
    fileName: "audio1",
    firstName: "mike",
    Surname: "peterson",
    propertyDate: "10-22-1967",
    propertySelect: "A",
    propertyDropdown: 2,
  },
  {
    fileName: "audio1",
    firstName: "mike",
    Surname: "peterson",
    propertyDate: "10-22-1967",
    propertySelect: "B",
    propertyDropdown: 2,
  }
]);
//onMounted(() => console.log(gridData.value))
</script>
<style>
</style>
