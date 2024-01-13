<template>
  <div>
    <nav class="navbar">
      <div class="container-fluid">
        <a class="navbar-brand">
          <img
            src="../assets/SymLogo.jpg"
            height="40"
            class="logo"
          />
          <p class="title" style="margin-left: 30px; margin-top: -35px">
            &nbsp;&nbsp;&nbsp;&nbsp;Title Form
          </p>
        </a>
        <ul class="nav">
          <div class="navbar-brand">
            <a href="https://www.youtube.com/">
              <img
                class="mata"
                src="../assets/eye.png"
                href="www.youtube.com"
                style="height: 25px; border-radius: 50px; margin-right: 18px"
              />
            </a>
          </div>
          <button
            type="button"
            class="btn btn-danger"
            data-bs-toggle="modal"
            data-bs-target="#exampleModal"
          >
            Submit
          </button>
          <div class="navbar-brand">
            <a href="https://www.youtube.com/">
              <img
                class="akun"
                src="../assets/akun.png"
                style="height: 30px; border-radius: 50px; margin-left: 30px"
              />
            </a>
          </div>
        </ul>
      </div>
      <ul class="nav justify-content-center" style="margin: 0 auto">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="/questions"
            >Questions</a
          >
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/responses">Responses</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/settings">Settings</a>
        </li>
      </ul>
    </nav>
    <div class="container">
      <legend>
        <h3>Title Form</h3>
      </legend>
      <div class="mb-3">
        <label for="formFile" class="form-label">Form discription</label>
        <input class="form-control" type="file" id="formFile" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
};
</script>
<style>
body {
  background-color: #fac0c1;
}
.navbar {
  background-color: #ffffff;
  border-bottom-right-radius: 15px;
  border-bottom-left-radius: 15px;
  width: 100%;
  padding: 40px;
  padding-bottom: 5px;
}
.navbar-brand {
  color: black;
}
.nav-link {
  color: black;
}

.btn-danger {
  background-color: #c43235;
  width: 103px;
  height: 40px;
  left: 1228px;
  top: 34px;
}
.container {
  background-color: #ffffff;
  align-items: center;
  margin-top: 80px;
  border-bottom-right-radius: 10px;
  border-bottom-left-radius: 10px;
  border-top-right-radius: 10px;
  border-top-left-radius: 10px;
  width: 60%;
  padding: 20px;
}
@media screen and (max-width: 992px) {
  .logo {
    height: 30px;
    margin-left: -30px;
    margin-top: -30px;
  }
  .title {
    font-size: 15px;
    margin-left: -30px;
  }
}
</style>