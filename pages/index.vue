<template>
    <div class="container">
        <div class="row align-items-center" style="padding-top: 80px">

            <div class="col-lg-6">
                <h1>QuitStat</h1>
                <p class="lead mt-5 mb-8">Thinking about having to keep track of whatever you Quit?? The amount of time
                    you have done without it and the total amount of money saved from that?? You do not have to
                    worry anymore.</p>
                <p>
                    <nuxt-link to="/register" v-if="!authenticated">
                        <button type="button" class="btn btn-lg btn-info" style="border-radius: 50px">Get Started
                        </button>
                    </nuxt-link>
                </p>
            </div>

            <div class="col-lg-5 ml-auto d-none d-lg-block">
                <img src="@/assets/img/clock.png" alt="img" style="width: 310px">
            </div>

        </div>
    </div>
</template>

<script>
    import Logo from '~/components/Logo.vue'

    export default {
        components: {
            Logo
        }
    }
</script>
