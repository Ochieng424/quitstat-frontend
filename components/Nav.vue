<template>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <nuxt-link class="nav-brand" to="/">QuitStat</nuxt-link>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav">
                <li class="nav-item">
                    <nuxt-link class="nav-link" to="/">Home</nuxt-link>
                </li>
                <li class="nav-item">
                    <nuxt-link class="nav-link" to="/about">About</nuxt-link>
                </li>
            </ul>
            <ul class="navbar-nav ml-auto">
                <li class="nav-item">
                    <nuxt-link class="nav-link" to="/login" v-if="!authenticated">Log In</nuxt-link>
                </li>
                <li class="nav-item">
                    <nuxt-link class="nav-link" to="/register" v-if="!authenticated">Register</nuxt-link>
                </li>
                <li class="nav-item dropdown mr-5" v-if="authenticated">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                        {{user.name}}
                    </a>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                        <a class="dropdown-item" href="#">Quit List</a>
                        <a class="dropdown-item" href="#">Profile</a>
                        <div class="dropdown-divider"></div>
                        <a class="dropdown-item" href="#" @click.prevent="logout()">Logout</a>
                    </div>
                </li>
            </ul>
        </div>
    </nav>
</template>

<script>
    export default {
        name: "Nav",
        methods:{
            logout(){
                this.$auth.logout();
            }
        }
    }
</script>

<style scoped>

</style>