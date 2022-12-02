<template>
    <div class="container">
        <div class="row">
            <div class="col-md-4">
                <div class="card shadow-lg">
                   <div class="card-body">
                    <p class="h3 display-3">{{this.count}}</p>
                    <button @click="incr" type="button" class="btn btn-success m-1">Increment</button>
                    <button @click="decr" type="button" class="btn btn-danger m-1">Decrement</button>
                   </div> 
                </div>
            </div>
        </div>
    </div>
</template>


<script>
export default {
    name: "CounterComponent",
    data: function() {
        return {
            count: 0
        }
    },
    methods : {
        incr : function() {
            this.count = this.count + 1;
        },

        decr : function() {
            this.count = this.count - 1;
        },

        by2 : function() {
            this.count = this.count * 2;
        }
    }
};
</script>


<style scoped>


</style>