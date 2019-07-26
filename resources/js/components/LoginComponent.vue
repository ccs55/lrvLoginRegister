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

      <form action method="POST">
        <div class="form">
          <p>Email address</p>
          <input type="text" placeholder="Enter your email" />

          <p>Password</p>
          <input type="text" placeholder="Enter your password" />

          <label class="check">
            Remember me
            <input type="checkbox" />
            <span class="checkmark"></span>
          </label>
        </div>
        <input type="submit" value="Log In" />
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




