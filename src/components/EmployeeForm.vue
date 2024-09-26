<template>
    <div id="employee-form">
        <h2>Add Employee</h2>
        <form @submit.prevent="submitForm"> <!-- Prevent default submission -->
            <div class="form-group">
                <label for="name">Name:</label>
                <input type="text" id="name" v-model="employee.name" required />
            </div>
            <div class="form-group">
                <label for="email">Email:</label>
                <input type="email" id="email" v-model="employee.email" required />
            </div>
            <button type="submit" class="btn">Add Employee</button>
        </form>
    </div>
</template>

<script>
export default {
    name: "employee-form",
    data() {
        return {
            employee: {
                name: "",
                email: "",
            },
        };
    },
    methods: {
        submitForm() {
            
            // Emit the new employee data to the parent component
            this.$emit("add:employee", this.employee);
            console.log("add employee",this.employee)

            // Reset the form fields
            this.employee = {
                name: "",
                email: "",
            };
        },
    },
};
</script>

<style scoped>
#employee-form {
    max-width: 500px;
    margin: 20px auto;
    padding: 20px;
    background-color: #f9f9f9;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

h2 {
    text-align: center;
    color: #333;
    margin-bottom: 20px;
}

.form-group {
    margin-bottom: 15px;
}

label {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
}

input[type="text"],
input[type="email"] {
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
    font-size: 16px;
}

.btn {
    background-color: #4CAF50;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    width: 100%;
    font-size: 16px;
}

.btn:hover {
    background-color: #45a049;
}
</style>