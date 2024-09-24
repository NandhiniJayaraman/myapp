<template>

<div id="employee-table">
    <table>
    <thead>
        <tr>
            <th>#</th>
            <th>Name</th>
            <th>Position</th>
            <th>Department</th>
            <th>Contact</th>
        </tr>
    </thead>
    <tbody>
        <tr v-for="employee in employees" :key="employee.id">
            <td>{{ employee.name}}</td>
            <td>{{employee.email}}</td>
        </tr>
    </tbody>
</table>

</div>
    
</template>


<script>
export default {
    name: "employee-table",
    props:{
        employess:Array
    }
}
</script>

<style scoped>
    #employee-table {
        max-width: 800px; /* Set a max width for the table container */
        margin: 20px auto; /* Center the table horizontally */
        padding: 20px;
        background-color: #f9f9f9; /* Light background for the container */
        border-radius: 10px; /* Rounded corners */
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Subtle shadow */
    }

    table {
        width: 100%; /* Full width table */
        border-collapse: collapse; /* Remove default cell spacing */
        margin-bottom: 20px; /* Add space below the table */
        font-family: Arial, sans-serif; /* Font */
    }

    th, td {
        padding: 12px 15px; /* Padding inside table cells */
        text-align: left; /* Align text to the left */
        border-bottom: 1px solid #ddd; /* Light border below rows */
    }

    th {
        background-color: #4CAF50; /* Green background for header */
        color: white; /* White text for header */
        font-weight: bold; /* Bold header text */
    }

    tr:nth-child(even) {
        background-color: #f2f2f2; /* Alternate row background */
    }

    tr:hover {
        background-color: #e0e0e0; /* Row hover effect */
    }
</style>
