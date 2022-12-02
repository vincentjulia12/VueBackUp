<template>
  <div class="container">
    <div class="row">
      <div class="col-md-5">
        <div class="card shadow-lg">
          <div class="card-body">
            <p class="h3">Hello {{msg}}</p>
            <button type="button" @click="greet(user.g)" class="btn btn-success m-1">Morning</button>
            <button type="button" @click="greet(f)" class="btn btn-warning m-1">Afternoon</button>
            <button type="button" @click="greet(i)" class="btn btn-danger m-1">Evening</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "GreetingComponent",
  data() {
    return {
      msg: "",
      user: {
        g: "tanginamo karl",
        f: "tasadas",
        i: "sfgsfgs"
      }
    }
  },
  methods: {
    greet(value) {
      this.msg = value;
    },

     pakyu() {
      this.msg = 'morning';
      console.log("hehe");
    }
  }
};
</script>

<style>

</style>