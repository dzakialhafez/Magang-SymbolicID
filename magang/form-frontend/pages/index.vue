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
          <b-card class="card-opening-box">
            <b-card-text>Sign in with</b-card-text>
            <NuxtLink to="/signin">
              <img src="~/assets/images/logo.png" alt="">
            </NuxtLink>
          </b-card>
        </div>
      </div>
    </b-row>
  </b-container>
</template>

<script>
export default {
  name: 'IndexPage'
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
  height: 100%;
  width: 100%;
  background-color: #464646;
  position: absolute;
  z-index: -2;
}
.card-opening{
  height: 550px;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
h1{
  color: white;
}
.card-opening-box{
  margin-top: 50px;
  background-color: rgb(255, 255, 255);
  width: 425.8px;
  padding: 15px;
  border-radius: 10px;
}

@media screen and (max-width: 500px) {
  .card-opening-box{
      width: 325.8px;
  }
}
</style>
