<template>
  <div class="container">
    <div class="row">
      <div class="col">
        <p class="h3">Customer</p>
        <ul class="list-group">
          <li class="list-group-item mt-1">
            Name: {{name}}
          </li>
          <li class="list-group-item">
            Age: {{age}}
          </li>
          <li class="list-group-item mb-4">
            Designation: {{designation}}
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CustomerComponent",
  props: {
    name : {type : String, required: true},
    age : {type : Number, required: true},
    designation : {type : String, required: true}
  }
}
</script>

<style>

</style>