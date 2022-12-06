<template>
    <div class="container">
        <div class="row">
            <div class="col mt-5 mb-2">
                <p id="p1" class="h3">User List</p>
            </div>
            <div v-if="loading === true">
                <SpinnerComponent/>
            </div>
            <div v-if="erroMessage">
                <p id="error-message">{{erroMessage}}</p>
            </div>
            <div v-after="3000" class="row" v-if="!loading && users.length > 0">
                <div class="col">
                    <table class="table table-hover text-center ">
                        <thead class="bg-dark text-white">
                            <tr>
                                <th>no.</th>
                                <th>Name</th>
                                <th>Email</th>
                                <th>Compony</th>
                                <th>Website</th>
                                <th>Location</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr v-for="user of users" :key="user.id">
                                <td>{{user.id}}</td>
                                <td>{{user.name}}</td>
                                <td>{{user.email}}</td>
                                <td>{{user.company.name}}</td>
                                <td>{{user.website}}</td>
                                <td>{{user.address.city}}</td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
 /* eslint-disable */
import { UserService } from '@/services/UserService';
import SpinnerComponent from './SpinnerComponent.vue';


export default {
  components: { SpinnerComponent },
    name: "UserListComponent",

    data() {
        return {
            loading: false,
            users: [],
            erroMessage: null
        };
    },
    created: async function() {
        try {
           this.loading = true;
           let response = await UserService.getAllUsers();
           setTimeout(() => {
                this.loading = false;
                this.users = response.data;  
                console.log('hello')
           }, 5000);
           
           
           
        } 
        
        catch(error) {
            this.loading = false;
            this.erroMessage = error;
        }
    } 
}
</script>

<style>

</style>