<template>
    <!-- <pre>{{isLoggedIn}}</pre> -->
    <div class="container">
        <div class="row">
            <div class="col-md-6">
                <div class="card">
                    <div class="card-body">
                        <div id="div-1" v-if="isLoggedIn">
                            <p id="p1" class="h3">Welcome User</p>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Autem debitis qui deleniti, molestiae voluptatibus quis. Est explicabo consequuntur culpa quidem repellendus animi, provident optio nisi nobis libero enim vitae ipsa.</p>
                        </div>
                        <div id="div-2" v-if="!isLoggedIn">
                            <p id="" class="h3 text-danger">Thank you</p>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Autem debitis qui deleniti, molestiae voluptatibus quis. Est explicabo consequuntur culpa quidem repellendus animi, provident optio nisi nobis libero enim vitae ipsa.</p>
                        </div>
                        <div id="main-container">
                            <div id="left-section">
                                <button v-if="!isLoggedIn" class="btn btn-success btn-sm m-1" @click="login()">Login</button>
                            </div>
                            <div id="right-section">
                                <button v-if="isLoggedIn" class="btn btn-danger btn-sm m-1 " @click="logout()">Logout</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    name: "AuthUserComponent",
    data(){
        return {
            isLoggedIn: false 
        };
    },
    methods: {
        login() {
            this.isLoggedIn = true;
        },
        logout() {
            this.isLoggedIn = false;
        }
    }
};
</script>

<style lang="scss">
@import "../style/main.scss"
</style>