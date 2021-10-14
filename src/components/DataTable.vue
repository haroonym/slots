<template>
  <div class="data-table">
    <h2><slot name="header"></slot></h2>
    <table>
      <thead>
        <tr>
          <th v-for="h of headers" :key="h">{{ h.text }}</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="i of items" :key="i">
          <td>{{ i.dessert }}</td>
          <td>{{ i.calories }}</td>
          <td>{{ i.fat }}</td>
          <td>{{ i.carbs }}</td>
          <td>{{ i.protein }}</td>
          <td>{{ i.iron }}</td>
        </tr>
        <slot name="body_content"></slot>
      </tbody>
    </table>
    <footer><slot name="footer"></slot></footer>
  </div>
</template>

<script>
export default {
  props: {
    items: {
      type: Array,
    },
    headers: {
      type: Array,
    },
  },
};
</script>

<style scoped>
.data-table {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-content: center;
  margin: 40px;
  border-collapse: collapse;
  font-size: 0.9em;
  font-family: sans-serif;
  min-width: 400px;
  box-shadow: 0 0 20px rgba(0, 0, 0, 0.15);
}
.data-table td,
th {
  text-align: left;
}
.data-table footer {
  margin: 30px 0 30px 0;
  font-style: italic;
}
.data-table thead tr {
  background-color: #009879;
  color: #ffffff;
  text-align: left;
}
.data-table th,
.data-table td {
  padding: 12px 15px;
}
.data-table tbody tr {
  border-bottom: 1px solid #dddddd;
}
.data-table tbody tr:nth-of-type(even) {
  background-color: #f3f3f3;
}
</style>
