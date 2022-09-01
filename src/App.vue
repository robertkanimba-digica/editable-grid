<template>
  <div class="container">
    <h3 class="p-3 text-center">item table</h3>
    <table class="table table-striped table-bordered">
      <thead>
        <tr>
          <th>fileName</th>
          <th>FirstName</th>
          <th>Surname</th>
          <th>propertyDate</th>
          <th>propertSelect</th>
          <th>propertDropdown</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="item in gridData.items" :key="item.id">
          <td>
            {{ item.fileName }}
            <input v-model="item.fileName" type="text" placeholder="edit me" />
          </td>
          <td>
            {{ item.firstName }}
            <input v-model="item.firstName" type="text" placeholder="edit me" />
          </td>
          <td>
            {{ item.Surname }}
            <input v-model="item.Surname" type="text" placeholder="edit me" />
          </td>
          <td>
            {{ item.propertyDate }}
            <input
              v-model="item.propertyDate"
              type="date"
              placeholder="edit me"
            />
          </td>
          <td>
            {{ item.propertySelect }}
            <select v-model="item.propertySelect" placeholder="edit me">
              <option disabled value="">Please select one</option>
              <option>A</option>
              <option>B</option>
              <option>C</option>
            </select>
          </td>
          <td>
            {{ item.propertyDropdown }}
            <select v-model="item.propertyDropdown" placeholder="edit me">
              <option disabled value="">Please select one</option>
              <option>A</option>
              <option>B</option>
              <option>C</option>
            </select>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script setup>
import { ref, onMounted } from "vue";
import GridComponent from "./components/GridComponent.vue";
import HelloWorld from "./components/HelloWorld.vue";

const gridColumn = ref([
  "fileName",
  "firstName",
  "Surname",
  "propertyDate",
  "propertySelect",
  "propertyDropdown",
]);
const gridData = ref({
  fields: [
    {
      key: "fileName",
      label: "File Name",
      type: "text",
      editable: true,
      placeholder: "Enter file name",
      class: "file-column",
    },
    {
      key: "firstName",
      label: "First Name",
      type: "text",
      editable: true,
      placeholder: "Enter First Name",
      class: "firstname-column",
    },
    {
      key: "surname",
      label: "Surnname",
      type: "text",
      editable: true,
      placeholder: "Enter Surname",
      class: "surname-column",
    },
    {
      key: "dateOfBirth",
      label: "Date Of Birth",
      type: "date",
      editable: true,
      placeholder: "Enter Name",
      class: "date-column",
    },
    {
      key: "propertySelect",
      label: "Random select",
      type: "select",
      editable: true,
      placeholder: "Select number",
      class: "select-column",
    },
    {
      key: "propertyDropdown",
      label: "DropDown Menu",
      type: "text",
      editable: true,
      placeholder: "Select option",
      class: "dropdown-column",
    },
  ],
  items: [
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
    },
  ],
});
//onMounted(() => console.log(gridData.value))
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
input,
select,
.gridData {
  display: block;
  padding: 10px 6px;
  width: 100%;
  box-sizing: border-box;
  border: none;
  border-bottom: 1px solid #ddd;
  color: #555;
}
ol {
  background: #ff9999;
  padding: 20px;
}

ul {
  background: #3399ff;
  padding: 20px;
}

ol li {
  background: #ffe5e5;
  color: darkred;
  padding: 5px;
  margin-left: 35px;
}

ul li {
  background: #cce5ff;
  color: darkblue;
  margin: 5px;
}
table {
  font-family: Arial, Helvetica, sans-serif;
  color: #666;
  font-size: 12px;
  text-shadow: 1px 1px 0px #fff;
  background: #eaebec;
  margin: 20px;
  border: #ccc 1px solid;

  -moz-border-radius: 3px;
  -webkit-border-radius: 3px;
  border-radius: 3px;

  -moz-box-shadow: 0 1px 2px #d1d1d1;
  -webkit-box-shadow: 0 1px 2px #d1d1d1;
  box-shadow: 0 1px 2px #d1d1d1;
}
table th {
  padding: 21px 25px 22px 25px;
  border-top: 1px solid #fafafa;
  border-bottom: 1px solid #e0e0e0;

  background: #ededed;
  background: -webkit-gradient(
    linear,
    left top,
    left bottom,
    from(#ededed),
    to(#ebebeb)
  );
  background: -moz-linear-gradient(top, #ededed, #ebebeb);
}
table tr {
  text-align: center;
  padding-left: 20px;
}
table td {
  padding: 18px;
  border-top: 1px solid #ffffff;
  border-bottom: 1px solid #e0e0e0;
  border-left: 1px solid #e0e0e0;

  background: #fafafa;
  background: -webkit-gradient(
    linear,
    left top,
    left bottom,
    from(#fbfbfb),
    to(#fafafa)
  );
  background: -moz-linear-gradient(top, #fbfbfb, #fafafa);
}
</style>
