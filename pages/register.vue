<template>
    <div class="container-fluid">
        <div class="row justified-content-center">
            <div class="col-sm-5 ml-auto mr-auto"
                 style="margin-top: 50px; background-color: #f4f4f4; padding: 0 50px 50px 50px; border-radius: 3px;">
                <h4>Register</h4>
                <form @submit.prevent="submit()">
                    <div class="form-group">
                        <label>Name</label>
                        <input v-model="form.name" type="text" class="form-control" placeholder="Enter name" autofocus>
                        <small class="form-text text-danger" v-if="errors.name">{{errors.name[0]}}</small>
                    </div>
                    <div class="form-group">
                        <label>Email address</label>
                        <input v-model.trim="form.email" type="email" class="form-control" placeholder="Enter email">
                        <small class="form-text text-danger" v-if="errors.email">{{errors.email[0]}}</small>
                    </div>
                    <div class="form-group">
                        <label>Password</label>
                        <input v-model.trim="form.password" type="password" class="form-control" placeholder="Password">
                        <small class="form-text text-danger" v-if="errors.password">{{errors.password[0]}}</small>
                    </div>
                    <button type="submit" class="btn btn-primary" style="width: 100%;">Register</button>
                </form>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "register",
        data() {
            return {
                form: {
                    name: '',
                    email: '',
                    password: ''
                }
            }
        },
        methods:{
            async submit(){
                await this.$axios.$post('register', this.form);
                await this.$auth.loginWith('local', {
                    data:{
                        email: this.form.email,
                        password: this.form.password
                    }
                });

                this.$router.push('/');
            }
        }
    }
</script>

<style scoped>

</style>