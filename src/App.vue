<template>
<div>

  <h1 class="Heading"> Employees </h1>

   <employee-table/>

</div>


</template>

<script>

import EmployeeTable from './components/EmployeeTable.vue'

export default {
  name: 'App',
  components: {
    EmployeeTable
    
  }
}
</script>

<style>
.Heading{
  color: #000;
  font-size: xx-large;
  text-align: center;
}

</style>
