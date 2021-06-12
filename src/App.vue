<script>
import Header from '@/components/Header.vue';
import Product from '@/components/Product.vue';
import Detail from '@/components/Detail.vue';
import { ref } from 'vue';

export default {
  components: {
    Header,
    Product,
    Detail
  },
  setup(){

    const checkForm = (event) => {
      const form = document.querySelector('#form1');
      // const form_register = document.querySelectorAll('.form-register');
      // const checkFormValidate = ref(true);
      // console.log(form_register);
      // console.log(form.checkValidity());
      // form_register.forEach(element => {
      //   if(element.type === "email"){
      //     if(!(element.value.length>=3 && ( 0 < element.value.indexOf("@") < element.value.length-1) && (element.value.indexOf(" ") === -1))){
      //       checkFormValidate.value = false;
      //     }
      //   }else{
      //     if (!element.value){
      //       checkFormValidate.value = false;
      //     }
      //   }
      // });
      // if(!checkFormValidate.value){
      //   form.classList.add('was-validated');
      //   event.preventDefault();
      // }
      if(!form.checkValidity()){
        form.classList.add('was-validated');
        event.preventDefault();
      }

      return true;

    }



    return { checkForm }
  }
  
}
</script>

<template>
  <!-- <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </div>
  <router-view/> -->
  <div>
    <!-- navbar -->
    <Header />
    <!-- breadcrumb -->

    <!-- 產品介紹 -->
    <Product />
    
    <!-- 產品詳情 -->
    <Detail />
    <div class="position-sticky bottom-0" style="z-index: 999">
    <button class="
            btn btn-warning btn-warning-hover btn-lg
            px-5
            fw-bold
            rounded-0
            mt-2
            w-100
            d-md-none
          " onclick="goForm()" id="bottomBtn">
      贊助專案
    </button>
  </div>
    <footer class="py-5 text-center">
      <div class="container">
        <small class="text-muted">YuLin | Copyright ©2021 美夢製造所 All rights reserved.</small>
      </div>
    </footer>

    <div class="modal" tabindex="-1" id="login">
  <div class="modal-dialog modal-dialog-centered">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title">登入</h5>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body">
        <form id="form1" class="needs-validation" @submit="checkForm" novalidate>
          <div>
            <label for="mail" class="form-label">帳號</label>
            <input type="email" id="mail" class="form-control form-register" required />
            <div class="invalid-feedback">請輸入帳號</div>
          </div>
          <div>
            <label for="password" class="form-label mt-3">密碼</label>
            <input type="password" id="password" class="form-control form-register" required />
            <div class="invalid-feedback">請輸入密碼</div>
          </div>
          <a href="#" class="text-muted d-block fs-sm mt-2 mb-3">忘記密碼？</a>
          <button type="submit" class="
                  btn btn-warning btn-warning-hover
                  w-100
                  rounded-pill
                  mb-3
                ">
            登入
          </button>
        </form>
        <div class="position-relative my-4">
          <div class="progress" style="height: 1px">
            <div class="progress-bar" role="progressbar" aria-valuenow="0" aria-valuemin="0" aria-valuemax="100"></div>
          </div>
          <div class="
                  position-absolute
                  top-0
                  start-50
                  translate-middle
                  bg-white
                  text-center text-muted
                  px-2
                  fs-sm
                ">
            還沒有帳號？<a href="#" class="link-danger">註冊一個帳號</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>




  </div>
  



</template>

<style lang="scss" scoped>
/*
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}*/
/* http://meyerweb.com/eric/tools/css/reset/ 
   v2.0 | 20110126
   License: none (public domain)
*/
.btn-warning-hover:hover{
  background-color: #FF785E;
  color: #fff;
  border-color: #FF785E;
}



</style>
