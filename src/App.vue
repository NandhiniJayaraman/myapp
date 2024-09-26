<template>
  <div>
    <h1 class="Heading">Employees</h1>

    <employee-form @add:employee="addEmployee" />

    <employee-table :employees="employees" />
  </div>
</template>

<script>
import EmployeeTable from './components/EmployeeTable.vue'
import EmployeeForm from "./components/EmployeeForm.vue"

export default {
  name: 'App',
  components: {
    EmployeeTable,
    EmployeeForm
  },
  data() {
    return {
      employees: [
        {
          id: 1,
          name: 'Kiruba',
          email: 'kiruba@gmail.com'
        },
        {
          id: 2,
          name: 'Nandhini',
          email: 'nansjayaraman@gmail.com'
        },
        {
          id: 3,
          name: 'Jasmine',
          email: 'jasmine@gmail.com'
        }
      ]
    };
  },
  methods: {

    addEmployee(data) {

      // const lastId = this.employees.length > 0 ? this.employees[this.employees.length - 1].id : 0;

      //       const id = lastId + 1;

      //       const newEmployee = {     ...this.employee, id:id    };
      //       console.log('new employees',newEmployee)
      
      // Add the new employee to the list
      console.log(data)
      this.employees = [...this.employees,data];
    }
  }
};
</script>

<style>
.Heading {
  color: #000;
  font-size: xx-large;
  text-align: center;
}
</style>
