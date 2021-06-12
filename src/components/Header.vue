<script>
export default {

}
</script>

<template>
  <header class="border-bottom border-5 border-warning">
      <div class="container">
        <nav class="navbar navbar-expand-lg navbar-light">
          <div class="container-fluid">
            <a class="navbar-brand" href="#">
                <img src="https://ecjia.com.tw/demo/bs5_homework_0526/assets/logo.jpg" alt="Logo">
            </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
              <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
              <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                <li class="nav-item">
                  <a class="nav-link active" aria-current="page" href="#">關於</a>
                </li>
                <li class="nav-item">
                  <a class="nav-link" href="#">挖寶</a>
                </li>
                <li class="nav-item">
                  <a class="nav-link" href="#">我有個大膽的想法</a>
                </li>
              </ul>
              <div>
                <a href="#" class="btn btn-outline-warning btn-outline-warning-hover rounded-pill ps-3 pe-3 pb-2 ms-1 me-1 border-2"  data-bs-toggle="modal" data-bs-target="#login">登入</a>
                <a href="#" class="btn btn-outline-secondary btn-outline-secondary-hover rounded-pill ps-3 pe-3 ms-1 me-1 border-2">註冊</a>
              </div>
            </div>
          </div>
        </nav>
      </div>
    </header>
</template>

<style lang="scss" scoped>
img {
    width: 111px;
    height: 40px;
}

.btn-outline-warning-hover:hover{
  background-color: #FF785E;
  color: #fff;
    border-color: #FF785E;
}

.btn-outline-warning{
    
    color: #858377;;
    // background: #FF785E;
}
.btn-outline-secondary{
}

.btn-outline-secondary-hover:hover{
  color: #fff;
}

// .btn-outline-secondary{
//     color: #858377;
// }




</style>