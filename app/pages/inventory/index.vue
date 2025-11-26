<template>
  <div>
  <v-card
    title="Inventory"
    rounded="50"
    
  >
    <template v-slot:text>
      <v-text-field
        v-model="search"
        label="Search"
        prepend-inner-icon="mdi-magnify"
        variant="outlined"
        hide-details
        single-line
      ></v-text-field>
    </template>

    <v-data-table
      :headers="headers"
      :items="inventory.data"
      :search="search"
    ></v-data-table>
  </v-card>
  </div>
</template>

<script setup>
  import { ref } from 'vue'

  const search = ref('')
  
  const { data: inventory} = await useFetch('http://localhost:1337/api/inventories');

  const headers = [
  
    { key: 'product_name', title: 'Inventory' },
    { key: 'product_description', title: 'Description' },
    { key: 'quantity', title: 'Quantity' },
    { key: 'unit', title: 'Unit' },
    { key: 'condition', title: 'Condition' },
    { key: 'location', title: 'Location' },
    { key: 'total_cost', title: 'Total Cost' },
    { key: 'remarks', title: 'Remarks' },
    { key: 'aquisition_cost', title: 'Cost' },
    
  ]

  
</script>


<style>

</style>

