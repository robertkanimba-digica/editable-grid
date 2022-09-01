<template>
  <form>
    <li>{{ myGrid.text }}</li>
  </form>
  <button @click="count++">you pressed me {{ count }} times</button>
</template>

  <script setup>
import { ref } from "vue";
const props = defineProps({
  myGrid: Object,
});
const count = ref(0);

function addNewItem() {
  var myObject = {
    fileName: this,
    firstName: "mike",
    Surname: "peterson",
    propertyDate: "10-22-1967",
    propertySelect: "B",
    propertyDropdown: 2,
  };
}
</script>