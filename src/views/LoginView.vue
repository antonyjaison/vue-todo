<template>
    <div class="login_section">
        <h1>
            join the <span>fun.</span>
        </h1>
        <div class="login_box">
            <form>
                <h1>Login</h1>
                <div>
                    <label> Name </label>
                    <input type="text" v-model="name">
                </div>
                <div>
                    <label> E-mail </label>
                    <input type="text" v-model="email">
                </div>
                <div>
                    <label> Password </label>
                    <input type="text" v-model="password">
                </div>
                <p>New to Roku Flashback? <router-link class="signup" to="/">Sign up now</router-link></p>
                <input type="submit" value="Register">
            </form>
        </div>
    </div>
</template>

<script>

export default {
    data() {
        return {
            name: '',
            email: '',
            password: ''
        };
    },
};

</script>

<style scoped>
.login_section {
    background-image: url('../assets/background.png');
    width: 100%;
    height: 100vh;
    background-size: cover;
    background-position: calc(-190px);
    display: flex;
    justify-content: space-around;
    align-items: center;
}

.login_section h1 {
    font-size: 70px;
    color: #fff;
    font-weight: bold;
}

.login_section h1 span {
    color: #E22998;
}

.login_box form {
    width: fit-content;
    height: fit-content;
    background-color: rgba(0, 0, 0, 0.4);
    border-radius: 10px;
    padding: 20px;
    display: flex;
    flex-direction: column;
    gap: 25px;
}
.login_box form p{
    color: #fff;
}

.login_box form div {
    display: flex;
    flex-direction: column;
    gap: 5px;
}

.login_box form div label {
    color: #fff;
    font-size: 18px;

}

.login_box form div input {
    width: 400px;
    height: 40px;
    border-radius: 5px;
    border: 3px solid #4FAAFF;
    background-color: transparent;
    color: #fff;
    font-size: 20px;
    padding-left: 10px;
}

.login_box form div input:focus {
    outline: none;
}
input[type="submit"]{
    width: 100%;
    height: 40px;
    background-color: #4ca7fd;
    color: #fff;
    font-size: 20px;
    border-radius: 5px;
    border: none;
    margin-top: 10px;
}

@media(max-width:430px) {
    .login_section {
        flex-direction: column;
        justify-content: center;
        gap: 20px;
    }

    .login_section h1 {
        font-size: 50px;
    }

    .login_box form {
        width: 350px;
        align-items: center;
    }
    .login_box form div label {
        font-size: 16px;
    }

    .login_box form div input {
        width: 300px;
    }
}
</style>