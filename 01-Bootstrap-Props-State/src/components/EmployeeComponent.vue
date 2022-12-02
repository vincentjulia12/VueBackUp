<template>
    <div class="container">
        <div class="row">
            <div class="col">
                <p class="h3">Employee</p>
                <ul class="list-group">
                    <li class="list-group-item">
                        Name: {{this.employee.name}}
                    </li>
                </ul>
                <ul class="list-group">
                    <li class="list-group-item">
                        Age: {{this.employee.age}}
                    </li>
                </ul>
                <ul class="list-group">
                    <li class="list-group-item">
                        Designation: {{this.employee.de}}
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "EmployeeComponent",
    data: function() {
        return {
            employee: {
                name: 'Vincent',
                age: 22,
                designation: 'gago'
            }
        }
    },
    props: {
        
    }
}
</script>

<style>

</style>