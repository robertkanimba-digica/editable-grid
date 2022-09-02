<template>
  <div>
    <grid-component :myGrid="gridData"></grid-component>
  </div>
</template>

<script setup>
import { ref } from "vue";
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
    surName: "peterson",
    date: new Date(1967, 3, 24),
    propertySelect: "C",
    propertyDropdown: 2,
  },
  {
    fileName: "audio1",
    firstName: "mike",
    surName: "peterson",
    date: new Date(1967, 3, 24),
    propertySelect: "A",
    propertyDropdown: 2,
  },
  {
    fileName: "audio1",
    firstName: "mike",
    surName: "peterson",
    date: new Date(1967, 3, 24),
    propertySelect: "B",
    propertyDropdown: 2,
  }
]);

</script>
<style>
</style>
