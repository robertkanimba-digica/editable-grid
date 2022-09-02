<template>
  <td>
    {{ props.rowData.fileName }}
    <input v-model="props.rowData.fileName" type="text" placeholder="edit me" />
  </td>
  <td>
    {{ props.rowData.firstName }}
    <input v-model="props.rowData.firstName" type="text" placeholder="edit me" />
  </td>
  <td>
    {{ props.rowData.Surname }}
    <input v-model="props.rowData.Surname" type="text" placeholder="edit me" />
  </td>
  <td>
    {{ props.rowData.propertyDate }}
    <input v-model="props.rowData.propertyDate" type="date" placeholder="edit me" />
  </td>
  <td>
    {{ props.rowData.propertySelect }}
    <select v-model="props.rowData.propertySelect" placeholder="edit me">
      <option disabled value="">Please select one</option>
      <option>A</option>
      <option>B</option>
      <option>C</option>
    </select>
  </td>
  <td>
    {{ props.rowData.propertyDropdown }}
    <select v-model="props.rowData.propertyDropdown" placeholder="edit me">
      <option disabled value="">Please select one</option>
      <option>A</option>
      <option>B</option>
      <option>C</option>
    </select>
  </td>
</template>

<script Setup>
import { defineProps } from "vue"
const props = defineProps({
  rowData: Object
})

</script>

<style>
</style>