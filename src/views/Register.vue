<template>
    <div class="Register">
        <h1>Đăng ký</h1>
        <form id="form-register">
            <input type="text" name="username" placeholder="Tài khoản"/> <br>

            <input type="text" name="email" placeholder="Email hoặc số điện thoại"/> <br>

            <input type="password" name="password" placeholder="Mật khẩu"/> <br>


            <input type="password" name="pw-again" placeholder="Nhập lại mật khẩu"/> <br>

            <button type="button" v-on:click="success()">Đăng ký</button>
            <button type="button" v-on:click="login()">Đăng nhập</button>
        </form>
    </div>
</template>

<script>
    export default {
        methods: {
            success() {
                alert("Bạn đã đăng ký thành công!")
            },
            login() {
                this.$router.push({ name: "login" });
            }
        } 
    }
</script>
<style>
    .Register {
        width: 500px;
        border: 1px solid #CCCCCC;
        background-color: #FFFFFF;
        margin: auto;
        margin-top: 160px;
        padding: 20px;
        border-radius: 10px;
        box-shadow: 5px 10px #006400;
    }

    .Register h1 {
        color: green;
        text-align: center;
    }


    #form-register input {
        width: 460px;
        margin-top: 20px;
        border-radius: 5px;
        padding: 8px;
    }

    #form-register button {
        margin-top: 20px;
        width: 100px;
        height: 40px;
        border-radius: 5px;
        background-color: #006400;
        margin-left: 70px;
        color: white;
    }
    
</style>