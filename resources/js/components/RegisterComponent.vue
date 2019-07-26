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

      <form action method="POST">
        <div class="form">
          <p>Full Name</p>
          <input type="text" placeholder="Enter your name" />

          <p>Email address</p>
          <input type="text" placeholder="Enter your email" />

          <p>Password</p>
          <input type="text" placeholder="Enter your password" />

          <label class="check">
            I accept
            <span id="accept">Terms and Conditions</span>
            <input type="checkbox" />
            <span class="checkmark"></span>
          </label>
        </div>
        <input type="submit" value="Sign Up" />
      </form>
    </div>

    <p class="footer">
      Already have an account?
      <span>
        <a href="/">Login</a>
      </span>
    </p>
  </div>
</template>

