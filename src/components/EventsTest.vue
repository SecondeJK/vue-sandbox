<template>
<div>
  Event Testing Template
  <button
    @click=clickEvent.action>
    Event Button
  </button>
  <table v-if="customValidate">
    <thead>
      <tr>
        <th v-for="header in tableHeaders">
          {{ header }}
        </th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="row in tableData">
        <td v-for="cellValue in row">
          {{ cellValue }}
        </td>
      </tr>
    </tbody>
  </table>
</div>

</template>

<script>
export default {
  name: 'EventsTest',
  props: {
    clickEvent: Object,
    tableHeaders: {
      type: Array,
      validator(value) {
        return true;
      }
    },
    tableData: {
      type: Array,
      required: true
    }
  },
  data: () => {
    return {
      customValidate: false
    }
  },
  created() {
    console.log("Created Component")
  },
  mounted: () => {
    console.log("Mounted Component");
  },
}
</script>
