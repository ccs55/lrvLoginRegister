<template>
  <div>
    <div id="register">
      <div class="simulor">
        <div class="logo">
          <h2>
            <img src="image/logo.PNG" alt />SIMULOR
          </h2>
        </div>
        <p class="create">Don't have an account? Create free account</p>
      </div>

      <form method="POST" action @submit.prevent="onSubmit">
        <div class="form">
          <p>Full Name</p>
          <input type="text" placeholder="Enter your name" name="name" v-model="user.name" />

          <p>Email address</p>
          <input type="text" placeholder="Enter your email" name="email" v-model="user.email" />

          <p>Password</p>
          <input
            type="password"
            placeholder="Enter your password"
            name="password"
            v-model="user.password"
          />

          <label class="check">
            I accept
            <span id="accept">Terms and Conditions</span>
            <input type="checkbox" />
            <span class="checkmark"></span>
          </label>
        </div>
        <input type="submit" value="Sign Up" />
        <p v-if="check">Đăng kí thành công !</p>
        <br />
      </form>
    </div>

    <p class="footer">
      Already have an account?
      <span>
        <a href="/login">Login</a>
      </span>
    </p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      user: {},
      check: false
    };
  },
  methods: {
    onSubmit() {
      axios.post("http://127.0.0.1:8000/users", this.user).then(response => {
        this.check = true;
      });
    }
  }
};
</script>
