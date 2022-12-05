<template>
  <div class="container">
    <div class="grid">
      <div class="row">
        <div class="col">
         
        </div>
      </div>
    </div>

    <UserListComponent/>
  </div>
  
</template>

<script>
import UserListComponent from "./components/UserListComponent.vue"

export default {
  name: 'App',
  components: {
    UserListComponent
  }
};
</script>

<style lang="scss">
@import "./style/main.scss";

</style>
