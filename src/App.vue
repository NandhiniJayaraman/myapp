<template>
<div>

  <h1 class="Heading"> Employees </h1>

   <employee-table  v-bind:employees= "employees" />

</div>


</template>

<script>

import EmployeeTable from './components/EmployeeTable.vue'

export default {
  name: 'App',
  components: {
    EmployeeTable
    
  },
  data(){
    return {

      employees:[
        {
          id:1,
          name:'Kiruba',
          email:'kiruba@gmail.com'
        },
          {
          id:2,
          name:'Nandhini',
          email:'nansjayaraman@gmail.com'
        },
          {
          id:3,
          name:'Jasmine',
          email:'jasmine@gmail.com'
        }
      ]

    }
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
