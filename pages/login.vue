<template>
    <div class="container-fluid">
        <div class="row justified-content-center">
            <div class="col-sm-5 ml-auto mr-auto"
                 style="margin-top: 50px; background-color: #f4f4f4; padding: 0 50px 50px 50px; border-radius: 3px;">
                <h4>Log In</h4>
                <form @submit.prevent="submit()">
                    <div class="form-group">
                        <label>Email address</label>
                        <input v-model.trim="form.email" type="email" class="form-control" placeholder="Enter email"
                               autofocus>
                        <small class="form-text text-danger">Error here.</small>
                    </div>
                    <div class="form-group">
                        <label>Password</label>
                        <input v-model.trim="form.password" type="password" class="form-control" placeholder="Password">
                        <small class="form-text text-danger">Error here.</small>
                    </div>
                    <button type="submit" class="btn btn-primary" style="width: 100%;">Login</button>
                </form>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "login",
        data() {
            return {
                form: {
                    email: '',
                    password: ''
                }
            }
        },
        methods: {
            // async submit() {
            //     await this.$auth.loginWith("local", {
            //         data: this.form
            //     })
            //
            //     this.$router.push('/');
            // }
        }
    }
</script>

<style scoped>

</style>