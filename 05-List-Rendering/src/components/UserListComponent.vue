<template>
    <div class="container">
        <div class="row">
            <div class="col">
                <p id="p1" class="h3">User List</p>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sapiente quam repudiandae animi aut eveniet quisquam, exercitationem maxime quasi nulla praesentium perferendis in velit perspiciatis sunt tempora ducimus pariatur dolores magnam.</p>
            </div>
            <div class="row">
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
import { UserService } from '@/services/UserService';

export default {
    name: "UserListComponent",
    data() {
        return {
            users: UserService.getAllUsers()
        }
    }
}
</script>

<style>

</style>