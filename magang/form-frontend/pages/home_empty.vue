<template>
  <div>
    <head>
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
    </head>
    <div class="header">
      <nav class="navbar">
        <div class="container-fluid">
          <span class="navbar-brand">
            <img
              src="../assets/images/sym.png"
              height="25px"
              class="d-inline-block align-text-top"
            />
            &nbsp;&nbsp;Symbolic Form
          </span>
          <ul class="nav">
            <div class="navbar-brand">
              <div class="dropdown dropdown-toggle"
              type="button"
              id="dropdownMenuButton1"
              data-bs-toggle="dropdown"
              aria-expanded="false"
              style="top: -3px;">
                <a href= "#">
                  <img
                    class="akun"
                    src="../assets/images/account.png"
                    style="height: 25px; border-radius: 50px; margin-left: 30px; background-color: white;"
                  />
                </a>
              </div>
              <ul class="dropdown-menu" aria-labelledby="dropdownMenuButton1">
                <li><a class="dropdown-item" href="#">Logout</a></li>
              </ul>
            </div>
          </ul>
        </div>
      </nav>

      <button type="button" class="btn btn-light">
        <div class="btn--icon">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            stroke-width="2"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M12 9v3m0 0v3m0-3h3m-3 0H9m12 0a9 9 0 11-18 0 9 9 0 0118 0z"
            />
          </svg>
        </div>
        <span class="btn--text">NEW FORM</span>
      </button>
    </div>

    <div v-if="form.length">
      <div class="container">
        <div class="row">
          <div class="col">
            <h3>My Form</h3>
          </div>
        </div>

        <div class="row row-cols-2 row-cols-md-4 g-4">
          <div class="col">
            <div class="card">
              <div class="card-header bg-transparent">
                <img class="cover" src="../assets/images/pic2.jpg" />
              </div>
              <div class="card-body text-success">
                <h5>Form Title 1</h5>
              </div>
              <div class="card-footer bg-transparent">
                <button class="pencil">
                  <img class="icon" src="../assets/images/pencil.jpg" />
                </button>
                <button class="eye">
                  <img class="icon" src="../assets/images/eye.jpg" />
                </button>
                <button class="comment">
                  <img class="icon" src="../assets/images/comment.jpg" />
                </button>
              </div>
            </div>
          </div>

          <div class="col">
            <div class="card">
              <div class="card-header bg-transparent">
                <img class="cover" src="../assets/images/pic2.jpg" />
              </div>
              <div class="card-body text-success">
                <h5>Form Title 2</h5>
              </div>
              <div class="card-footer bg-transparent">
                <button class="pencil">
                  <img class="icon" src="../assets/images/pencil.jpg" />
                </button>
                <button class="eye">
                  <img class="icon" src="../assets/images/eye.jpg" />
                </button>
                <button class="comment">
                  <img class="icon" src="../assets/images/comment.jpg" />
                </button>
              </div>
            </div>
          </div>

          <div class="col">
            <div class="card">
              <div class="card-header bg-transparent">
                <img class="cover" src="../assets/images/pic3.jpg" />
              </div>
              <div class="card-body text-success">
                <h5>Form Title 3</h5>
              </div>
              <div class="card-footer bg-transparent">
                <button class="pencil">
                  <img class="icon" src="../assets/images/pencil.jpg" />
                </button>
                <button class="eye">
                  <img class="icon" src="../assets/images/eye.jpg" />
                </button>
                <button class="comment">
                  <img class="icon" src="../assets/images/comment.jpg" />
                </button>
              </div>
            </div>
          </div>

          <div class="col">
            <div class="card">
              <div class="card-header bg-transparent">
                <img class="cover" src="../assets/images/pic4.jpg" />
              </div>
              <div class="card-body text-success">
                <h5>Form Title 4</h5>
              </div>
              <div class="card-footer bg-transparent">
                <button class="pencil">
                  <img class="icon" src="../assets/images/pencil.jpg" />
                </button>
                <button class="eye">
                  <img class="icon" src="../assets/images/eye.jpg" />
                </button>
                <button class="comment">
                  <img class="icon" src="../assets/images/comment.jpg" />
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="not-found" v-else>
      <img class="text-center">
      <img src="../assets/images/not-found.jpg" class="image mx-auto">
      </div>
      <p class="red">Blank Form</p>
      <p>You don't have any form</p>
  </div>
</template>

<script>
export default {
  name: 'BlankPage',
  data () {
    return {
      form: [

      ]
    }
  }
}
</script>

<style>
body{
  font-family: Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}
.navbar{
  background-color: #464646;
  color: #FFFFFF;
  border-bottom-right-radius: 15px;
  border-bottom-left-radius: 15px;
  width: 100%;
  padding: 20px;
  padding-bottom: 15px;
}
.navbar-brand{
  color: #FFFFFF;
}
.btn {
  display: flex;
  align-items: center;
  padding: 8px 16px;
  border-radius: 8px;
  border: 0;
  background-color: white;
  box-shadow: 0 4px 6px 0px rgba(0, 0, 0, 0.1),
    0 2px 4px -1px rgba(0, 0, 0, 0.06);
  margin-left: 600px;
  cursor: pointer;
  position: relative;
  top: -20px;
}
.btn--text {
  font-size: 0.8rem;
  font-weight: 500;
  margin-left: 8px;
}
.btn--icon {
  width: 24px;
  height: 24px;
}
.red,
p{
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  align-content: center;
}
.not-found{
  padding: 250px;
  margin-top: -150px;
}
.red {
  font-size: 20px;
  color: #C43235;
  margin-top: -180px;
}
p{
  font-size: 16px;
  color: #1d1b1b;
}
.image{
  display: block;
  width: 150px;
}
.cover{
  width: 200px;
  margin-left: -5px;
  margin-top: 5px;
  border-radius: 15px;
}
.card{
  width: 230px;
  height: 270px;
  border-radius: 15px;
  background-color: darkgrey;
  margin-left: 15px;
}
h3{
  font-size: 16px;
  margin-top: 30px;
  margin-bottom: 20px;
  font-weight: bold;
  margin-left: 15px;
}
h5{
  font-size: 16px;
  text-align: center;
  color: black;
  margin-top: -70px;
  background-color: #FFFFFF;
  border-radius: 15px;
  width: 200px;
  margin-left: -5px;
  padding-top: 10px;
  padding-bottom: 10px;
}
.icon{
  height: 20px;
}
.pencil,
.eye,
.comment{
  height: 20px;
  border-radius: 8px;
  border: 0;
  background-color: white;
  margin-right: 16px;
  margin-left: 10px;
}
.card-footer{
  border: 0px;
  margin-top: -25px;
}
.dropdown{
  border-radius: 50px;
  top: 20px;
}
@media screen and (max-width: 992px) {
.card{
  width: 130px;
  height: 170px;
  margin-left: 50px;
  margin-bottom: 50px;
}
h3{
  margin-left: 50px;
}
.cover{
  width: 115px;
  margin-left: -13px;
  margin-top: 1px;
}
h5{
  font-size: 14px;
  margin-top: -70px;
  width: 115px;
  margin-left: -13px;
  padding-top: 10px;
  padding-bottom: 10px;
}
.icon{
  height: 14px;
}
.pencil,
.eye,
.comment{
  height: 14px;
  border-radius: 8px;
  border: 0;
  background-color: white;
  margin-right: 0px;
  margin-left: 0px;
}
.card-footer{
  border: 0px;
  margin-top: -35px;

}
.btn {
  margin-left: 180px;
}
.red {
  font-size: 14px;
  color: #C43235;
  margin-top: -180px;
}
p{
  font-size: 14px;
  white-space: nowrap;
}
.not-found{
  padding: 250px;
  margin-top: -150px;
}
.image{
  display: block;
  width: 120px;
  left: -50px;
}
}

</style>
