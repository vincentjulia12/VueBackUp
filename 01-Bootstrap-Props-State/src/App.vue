<template>
  <div class="container">
    <div class="grid">
      <div class="row">
        <div class="col">
          <p id="p1" class="h3 mt-3">App Component</p>
          <p id="p2" class="">Lorem ipsum dolor sit amet consectetur adipisicing elit. Veritatis qui deserunt error. Culpa cum odio beatae libero accusamus, itaque facere minima consectetur voluptatibus optio molestias nemo porro asperiores magnam natus.</p>
        </div>
      </div>
    </div>

    <CustomerComponent name="Vincent" age="22" designation="gago"/>

    <EmployeeComponent/>
  </div>
  
</template>

<script>
import CustomerComponent from "./components/CustomerComponent.vue"
import EmployeeComponent from "./components/EmployeeComponent.vue"
export default {
  name: 'App',
  components: {
    CustomerComponent,
    EmployeeComponent
  }
}
</script>

<style lang="scss">
@import "./style/main.scss";

</style>
