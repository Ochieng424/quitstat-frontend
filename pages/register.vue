<template>
    <div class="container-fluid">
        <div class="row justified-content-center">
            <div class="col-sm-5 ml-auto mr-auto" style="margin-top: 50px; background-color: #f4f4f4; padding: 0 50px 50px 50px; border-radius: 3px;">
                <h4>Register</h4>
                <form>
                    <div class="form-group">
                        <label>Name</label>
                        <input type="text" class="form-control" placeholder="Enter name">
                        <small class="form-text text-danger">Error here.</small>
                    </div>
                    <div class="form-group">
                        <label>Email address</label>
                        <input type="email" class="form-control" placeholder="Enter email">
                        <small class="form-text text-danger">Error here.</small>
                    </div>
                    <div class="form-group">
                        <label>Password</label>
                        <input type="password" class="form-control" placeholder="Password">
                        <small class="form-text text-danger">Error here.</small>
                    </div>
                    <button type="submit" class="btn btn-primary" style="width: 100%;">Register</button>
                </form>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "register"
    }
</script>

<style scoped>

</style>