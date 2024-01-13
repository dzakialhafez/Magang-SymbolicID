<template>
  <b-container fluid>
    <b-row>
      <!-- Background -->
      <div class="bg">
        <div class="bg-merah"></div>
        <div class="bg-hitam"></div>
      </div>

      <!-- Card Login -->
      <div class="card-opening">
        <div class="text-center">
          <!-- welcome -->
          <h1>Welcome !</h1>

          <!-- Card Login Box -->
          <!-- Card Signin -->
          <div class="card-signin">
            <p>Sign in with</p>
            <b-form>
              <!-- Email -->
              <b-form-input
                type='email'
                placeholder="Email"
                required
                class="mt-2"
              >
              </b-form-input>

              <!-- Password -->
              <b-form-input
                type='password'
                placeholder="Password"
                required
                class="mt-2 mb-2"
              >
              </b-form-input>
               <b-button type="submit" variant="primary" class="mt-2 mb-2">Sign in</b-button>
            </b-form>
            <NuxtLink to="#" class="my-3">Forgot your password?</NuxtLink>
          </div>
          <p class="mt-3 registered">Not registered? <NuxtLink to="/signup">Sign up</NuxtLink></p>
        </div>
      </div>
    </b-row>
  </b-container>
</template>

<script>
export default {
  name: 'LoginPage'
}
</script>

<style scoped>
.bg-merah{
  height: 350px;
  width: 100%;
  background-image: linear-gradient(to right, #40A8C4, #5B73B5, #7441A7);
  position: absolute;
  z-index: -1;
}
.bg-hitam{
  height:100%;
  width: 100%;
  background-color: #464646;
  position: absolute;
  z-index: -2;
}
.card-opening{
  height: 650px;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
h1{
  color: white;
}
.card-signin{
  margin-top: 50px;
  background-color: rgb(255, 255, 255);
  width: 425.8px;
  padding: 15px;
  border-radius: 10px;
}
.registered{
  color: white;
}

@media screen and (max-width: 500px) {
  .card-signin{
      width: 325.8px;
  }
}
</style>
