<template>
  <div class="container">
    <h3 class="p-3 text-center">item table</h3>
    <table class="table table-striped table-bordered">
      <thead>
        <tr>
          <th>fileName</th>
          <th>FirstName</th>
          <th>Surname</th>
          <th>Date</th>
          <th>propertySelect</th>
          <th>propertDropdown</th>
        </tr>
      </thead>
      <tbody>
        <grid-row-component v-for="item in props.myGrid" :key="item.id" :rowData="item"></grid-row-component>
      </tbody>
    </table>
  </div>
</template>

  <script setup>
import GridRowComponent from "./GridRowComponent.vue";

const props = defineProps({
  myGrid: Array
});

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
  background: -webkit-gradient(linear,
      left top,
      left bottom,
      from(#ededed),
      to(#ebebeb));
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
  background: -webkit-gradient(linear,
      left top,
      left bottom,
      from(#fbfbfb),
      to(#fafafa));
  background: -moz-linear-gradient(top, #fbfbfb, #fafafa);
}
</style>