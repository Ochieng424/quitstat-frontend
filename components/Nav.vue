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
                    <nuxt-link class="nav-link" to="/login">Log In</nuxt-link>
                </li>
                <li class="nav-item">
                    <nuxt-link class="nav-link" to="/register">Register</nuxt-link>
                </li>
            </ul>
        </div>
    </nav>
</template>

<script>
    export default {
        name: "Nav"
    }
</script>

<style scoped>

</style>