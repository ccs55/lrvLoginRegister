<template>
  <div>
    <div id="login">
      <div class="simulor">
        <div class="logo">
          <h2>
            <img src="image/logo.PNG" alt />SIMULOR
          </h2>
        </div>
        <p class="create">Enter your email address and password to access admin panel.</p>
      </div>

      <form action method="POST" @submit.prevent="onSubmit">
        <div class="form">
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
            Remember me
            <input type="checkbox" />
            <span class="checkmark"></span>
          </label>
        </div>
        <input type="submit" value="Log In" />
        <p v-if="check_ok">Đăng nhập thành công !!!!!</p>
        <p v-if="check_fail">Đăng nhập thất bại !</p>
      </form>
    </div>
    <div class="footer">
      <p>Forgot your password?</p>
      <p class="footer">
        Already have an account?
        <span>
          <a href="/register">Sign Up</a>
        </span>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      user: {},
      check_ok: false,
      check_fail: false
    };
  },
  methods: {
    onSubmit() {
      axios
        .post("http://127.0.0.1:8000/users/login", this.user)
        .then(response => {
          var data = response.data.success;
          if (data > 0) {
            this.check_ok = true;
            this.check_fail = false;
          } else {
            this.check_ok = false;
            this.check_fail = true;
          }
        });
    }
  }
};
</script>





