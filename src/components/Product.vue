<script>

export default {

}
</script>

<template>
  <section class="py-5 bg-light">
      <div class="container">
        <div class="row">
          <div class="col-12 mb-4">
            <span class="badge bg-secondary">魔法科技</span>
            <h1 class="fz-32">拍出會動的照片｜LivePhotos 魔法拍立得</h1>
          </div>
          <div class="col-xl-7 col-lg-7 d-flex ">
            <img class="livePhoto" src="https://hexschool.github.io/boootstrap5WebLayout/assets/produt_image.jpg" alt="" />
            <!-- <div class="pic"><br><br><br><br><br><br><br><br><br><br></div> -->
          </div>
          <div class="col-xl-5 col-lg-5 d-flex align-items-center py-3">
            <div class="box w-100">
              <div>
                <h2 class="h6 text-muted mb-0 fz-14">目標 NTD$600,000</h2>
                <p class="h2 fz-32">$280,047</p>
                <div class="progress mb-2">
                  <div class="progress-bar bg-warning" role="progressbar" style="width: 80%;" aria-valuenow="80" aria-valuemin="00" aria-valuemax="100">80%</div>
                </div>
              </div>
            
            <!-- <div class="progress">
              <div class="progress-bar" role="progressbar" style="width: 25%;" aria-valuenow="25" aria-valuemin="0" aria-valuemax="100">25%</div>
            </div> -->
              <div class="row">
                <div class="col-xl-6 col-md-6">
                  <h2 class="h6 text-muted mb-0">贊助人數</h2>
                  <p class="h2 mb-3">1374人</p>
                </div>
                <div class="col-xl-6 col-md-6">
                  <h2 class="h6 text-muted mb-0">募資倒數</h2>
                  <p class="h2 mb-3">27天</p>
                </div>
                <div class="col-md-6 mb-3">
                  <ul class="d-flex justify-content-between justify-content-md-start list-unstyled">
                    <li class="custom-icons me-0 me-md-3">
                      <a href="#" class="link-dark text-decoration-none" data-bs-toggle="tooltip" data-bs-placement="top" title="認證標章" data-bs-customClass="mytooltip">
                        <img src="https://ecjia.com.tw/demo/bs5_homework_0526/assets/xunzhang.svg" alt="認證標章圖標" class="me-1" />
                        <small class="d-md-none align-bottom">認證標章</small></a>
                    </li>
                    <li class="custom-icons me-0 me-md-3">
                      <a href="#" class="link-dark text-decoration-none" data-bs-toggle="tooltip" data-bs-placement="top" title="品質保證" data-bs-customClass="mytooltip">
                        <img src="https://ecjia.com.tw/demo/bs5_homework_0526/assets/dianzan.svg" alt="品質保證圖標" class="me-1" />
                        <small class="d-md-none align-bottom">品質保證</small>
                      </a>
                    </li>
                    <li class="custom-icons me-0 me-md-3">
                      <a href="#" class="link-dark text-decoration-none" data-bs-toggle="tooltip" data-bs-placement="top" title="原生創意" data-bs-customClass="mytooltip">
                        <img src="https://ecjia.com.tw/demo/bs5_homework_0526/assets/tishi.svg" alt="原生創意圖標" class="me-1" />
                        <small class="d-md-none align-bottom">原生創意</small>
                      </a>
                    </li>
                    <li class="custom-icons">
                      <a href="#" class="link-dark text-decoration-none" data-bs-toggle="tooltip" data-bs-placement="top" title="人氣王" data-bs-customClass="mytooltip">
                        <img src="https://ecjia.com.tw/demo/bs5_homework_0526/assets/huangguan.svg" alt="人氣王圖標" class="me-1" />
                        <small class="d-md-none align-bottom">人氣王</small></a>
                    </li>
                  </ul>
                </div>
              </div>
            
            
              <div class="border-start border-warning border-3 bg-white p-2 mb-4">
                專案募資中！<br />
                在 2021/06/14 23:59 募資結束前，您都可以持續贊助此計畫。
              </div>
              <div class="row gx-3 mb-4">
                <div class="col-12">
                  <a href="#sponsor" class="btn btn-lg btn-warning rounded-pill btn-warning-hover w-100">贊助專案</a>
                </div>
              </div>
              <div class="row gx-3">
                <div class="col-6">
                  <!-- <a href="#" class="btn btn-lg btn-outline-secondary rounded-pill w-100"> -->
                  <a href="#" class="btn btn-lg btn-outline-secondary btn-outline-secondary-hover rounded-pill w-100">  
                    <i class="fas fa-heart custom-heart"></i>
                    追蹤專案</a>
                </div>
                <div class="col-6">
                  <a href="#" class="btn btn-lg btn-outline-secondary btn-outline-secondary-hover rounded-pill w-100">
                    <i class="fas fa-share-alt"></i>
                    追蹤專案</a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
</template>

<style lang="scss" scoped>
.btn-warning-hover:hover{
  background-color: #FF785E;
  color: #fff;
  border-color: #FF785E;
}
.btn-outline-secondary-hover:hover{
  border-color: #ffdf65;
  background: #ffdf65;
  .custom-heart{
    color: #FF785E;
  }
}

img{
  // border: 1px solid red;
  width: 100%;
}
.livePhoto{
  border-radius: 2rem;
}
.fz-32{
  font-size: 32px;
}
.fz-14{
  font-size: 14px;
}

.custom-icons {

  img{
    @media(max-width: 767.98px){
        width: 20px;
        height: 20px;
    }
  }
  
  // @media (min-width: 767.98px) { 
  //   display: flex;
  // }
  
}
</style>