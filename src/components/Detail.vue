<script>
import { ref } from 'vue';

export default {

  setup(){
    

    const checkForm = (event) => {
      const form = document.querySelector('#form');
      // const form_sponsor = document.querySelectorAll('.form-sponsor');
      // const checkFormValidate = ref(true);
      

      // form_sponsor.forEach(element => {
      //   if (!element.value){
      //     checkFormValidate.value = false;
      //   }
      // });
      // if(!checkFormValidate.value){
      //   form.classList.add('was-validated');
      //   event.preventDefault();  // 如果事件可以被取消，就取消事件。
      // }
      if(!form.checkValidity()){
        form.classList.add('was-validated');
        event.preventDefault();
      }
      
      return true;
    }

    const heightToTop = (ele)=> {
        let bridge = ele;
        let root = document.body;
        let height = 0;
        do {
            height += bridge.offsetTop;
            bridge = bridge.offsetParent;
        } while (bridge !== root);

        return height;
    }
    const goToTab =  () => {
      
      window.scrollTo({
        top: heightToTop(document.getElementsByClassName("tab-content")[0]) - 70,
        behavior: "smooth"
      });
      
    }


    return { goToTab, checkForm }
  }




}
</script>

<template>
  <section>
    <!-- fixed 選單 -->
    <div class="border-bottom border-top bg-white border-2 position-sticky" style="top:0; z-index: 1;">
      <div class="container">
        <!-- <div class="row"> -->
          <!-- links -->
          <!-- <div class="col-sm-12"> -->
            <ul class="nav d-md-flex justify-content-between justify-content-md-start" role="tablist" aria-orientation="vertical">
              <li class="nav-item">
                <a class="nav-link py-3 active" data-bs-toggle="pill" href="#tab-detail" role="tab" aria-controls="tab-detail" aria-selected="true"  @click="goToTab">專案介紹</a>
              </li>
              <li class="nav-item">
                <a class="nav-link py-3" data-bs-toggle="pill" href="#tab-news" role="tab" aria-controls="tab-news" aria-selected="false"  @click="goToTab">常見問答</a>
              </li>
              <li class="nav-item">
                <a class="nav-link py-3" data-bs-toggle="pill" href="#tab-qa" role="tab" aria-controls="tab-qa" aria-selected="false"  @click="goToTab">目前進度</a>
              </li>
              <li class="nav-item">
                <a class="nav-link py-3" data-bs-toggle="pill" href="#tab-comment" role="tab" aria-controls="tab-comment" aria-selected="false"  @click="goToTab">留言</a>
              </li>
            </ul>
          <!-- </div> -->
        <!-- </div> -->
      </div>
    </div>
      <div class="container">
        <div class="my-4">
          <div class="row g-5">
            <!-- 左邊 card 區塊 -->
            <div class="col-xxl-9 col-lg-8">
            
              <div class="tab-content mb-5">
                <!-- 專案介紹 -->
                <div class="tab-pane fade show active" id="tab-detail" role="tabpanel">
                  <img src="https://ecjia.com.tw/demo/bs5_homework_0526/assets/p1.jpg" alt="施了魔法的照片/文章示意圖" class="img-fluid w-100" />
                  <h2 class="mt-3 mb-1 ps-3 fs-4 border-start border-4 border-warning fw-bolder">
                    施了魔法的照片
                  </h2>
                  <p class="lh-lg text-justify mt-2">
                    受就相法大夠局來畫師我只這然以放灣得的後人心年我物我年，或人有動與次出女親構算帶年行著所間女，外成認心香吸工並知日成展源大超時動為生葉衣致長山對精做英密差家他微熱建取示濟定心一，品定把別銀動，深青輪一物加，生明果。西業白老如天有表非民大條全那遊，李文遊、像香過元學須本致信校態麼資司媽人價在它，地他不我計孩廠然不大指勢生的華常簡岸然，人著母病石金萬得一果。
                  </p>
                  <!-- <p>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorem rem esse iusto, cupiditate laborum fugit autem vero maiores in eaque placeat officia voluptate, neque iste corporis perferendis asperiores a dolorum eveniet accusantium quaerat pariatur velit error vitae? Eius rerum
                    voluptate dolores, cumque eos aperiam officiis porro nobis architecto voluptas temporibus nam debitis nisi quam. Nihil nobis quidem ipsam tenetur! Eveniet sit sint ratione perspiciatis obcaecati et porro eum distinctio in. Blanditiis earum a architecto exercitationem velit adipisci
                    nihil reprehenderit quasi, enim fugiat, esse magnam debitis, nemo sit nostrum corporis laboriosam. Libero provident non laboriosam quis culpa mollitia quam alias. Ratione pariatur laborum magnam dicta minima suscipit unde rem non possimus omnis praesentium modi blanditiis totam,
                    tenetur molestias harum repudiandae nihil maiores nemo minus quaerat quod aut doloremque natus! Laborum quae enim repudiandae ut culpa omnis atque architecto ab, harum facere doloremque similique, recusandae modi vitae. Dolorum reiciendis quod odit iste aut sequi. Praesentium
                    mollitia dolorem laboriosam dolor ipsam illum tempora nihil, repudiandae eos iste, explicabo ullam, delectus deserunt sit atque suscipit eligendi? Amet libero, laborum itaque sunt enim qui nam quia eius. Adipisci, ad veritatis, quos recusandae velit omnis asperiores dolor
                    voluptates incidunt officia commodi. Optio velit quisquam numquam nulla quia! Cupiditate perferendis doloremque laborum saepe tempora odit, esse ex quae iste veritatis consectetur dolorem nam aperiam, asperiores ducimus dicta neque! Alias maiores ut, in blanditiis ipsam eligendi.
                    Reprehenderit dolorem architecto blanditiis voluptatum neque cupiditate necessitatibus quia, ipsum eaque velit nulla accusamus aliquam recusandae, ut quae debitis atque mollitia rem voluptas tempora nemo magni sed cumque officiis. Eaque voluptas illum hic sed dignissimos eligendi
                    quisquam ad ipsum consectetur optio natus modi dolorem tenetur nam suscipit iusto assumenda saepe repellat sit, amet, voluptatibus minus. Labore excepturi facere incidunt repellat cupiditate ullam exercitationem eum non dolores sint, quidem quibusdam porro illum eligendi vero?
                    Optio velit vel incidunt itaque non voluptatibus corrupti tempora laborum necessitatibus aliquam expedita ab, minus sunt qui dolorum vero officia sint, dicta sapiente fuga inventore eligendi architecto unde. Voluptatem expedita, nesciunt maxime officia est aspernatur nisi
                    recusandae ad voluptatum veritatis quos cum exercitationem dicta fugit illo porro in velit dolorem perspiciatis et doloremque perferendis? Placeat amet numquam obcaecati quia. Eligendi animi nesciunt vero voluptate veniam adipisci odio. Temporibus fugiat voluptate dicta nulla
                    molestiae id accusamus fuga cum veritatis. Dolor, temporibus dolorem ullam amet accusamus voluptate aliquam rerum autem hic aperiam quam deserunt odit laudantium debitis atque dicta nisi rem natus error recusandae. Deleniti sunt cupiditate neque velit doloremque veniam, dolores
                    quos quod deserunt accusamus voluptatibus, perferendis dicta optio. Ea neque, in asperiores harum doloremque repellat, consequuntur rerum perspiciatis recusandae eum sapiente consectetur, aut voluptatum commodi error quae necessitatibus officia natus vel reprehenderit ut. Sapiente
                    animi consectetur ipsum perferendis ullam dolor officiis aperiam veritatis distinctio earum, corporis saepe. Accusantium consequatur vero soluta necessitatibus totam assumenda quo dolorum, ipsa quam neque hic recusandae, excepturi eum animi laborum nulla fuga ex labore vel.
                    Consectetur ratione placeat repellat ad necessitatibus rem sint optio sequi? Facere aperiam error possimus magnam est ut quod blanditiis.
                  </p> -->
                  <!-- <img src="https://fakeimg.pl/600x400" width="100%" alt="" /> -->
                  <img src="https://ecjia.com.tw/demo/bs5_homework_0526/assets/p2.jpg" alt="留下當下的美好/文章示意圖" class="img-fluid mt-4 w-100" />
                  <h2 class="mt-3 ps-3 border-start border-4 border-warning fw-bolder fs-4">留下當下的美好</h2>
                  <p class="lh-lg text-justify mt-2">
                    受就相法大夠局來畫師我只這然以放灣得的後人心年我物我年，或人有動與次出女親構算帶年行著所間女，外成認心香吸工並知日成展源大超時動為生葉衣致長山對精做英密差家他微熱建取示濟定心一，品定把別銀動，深青輪一物加，生明果。西業白老如天有表非民大條全那遊，李文遊、像香過元學須本致信校態麼資司媽人價在它，地他不我計孩廠然不大指勢生的華常簡岸然，人著母病石金萬得一果。
                  </p>
                </div>
                <!-- 最新消息 -->
                <div class="tab-pane fade" id="tab-news" role="tabpanel">
                  <ul class="list-unstyled accordion accordion-flush" id="qa-accordion">
                    <li class="accordion-item">
                      <h2 class="accordion-header" id="flush-headingOne">
                        <button class="accordion-button btn-outline-warning collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#flush-collapseOne" aria-expanded="false" aria-controls="flush-collapseOne">
                          <span class="
                                  bg-warning
                                  text-dark
                                  font-baloo-tamma
                                  fs-sm
                                  fw-bolder
                                  text-center
                                  rounded
                                  me-3
                                  pt-1
                                  lh-lg
                                  letter-spacing-7
                                  px-2
                                ">
                            Q1
                          </span>
                          影片拍完之後可以編輯嗎？
                        </button>
                      </h2>
                      <div id="flush-collapseOne" class="accordion-collapse collapse" aria-labelledby="flush-headingOne" data-bs-parent="#qa-accordion">
                        <p class="accordion-body mb-0 fs-sm lh-lg text-secondary">
                          可以進行簡易的編輯，內建 5
                          種濾鏡，影片秒數有3秒、5秒、10秒可以選擇，拍完的當下可以編輯要印出來的影片範圍哦！
                        </p>
                      </div>
                    </li>
                    <li class="accordion-item">
                      <h2 class="accordion-header" id="flush-headingTwo">
                        <button class="accordion-button btn-outline-warning collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#flush-collapseTwo" aria-expanded="false" aria-controls="flush-collapseTwo">
                          <span class="
                                  bg-warning
                                  text-dark
                                  font-baloo-tamma
                                  fw-bolder
                                  text-center
                                  rounded
                                  fs-sm
                                  me-3
                                  pt-1
                                  lh-lg
                                  letter-spacing-7
                                  px-2
                                ">
                            Q2
                          </span>
                          有提供保固或維修服務嗎？
                        </button>
                      </h2>
                      <div id="flush-collapseTwo" class="accordion-collapse collapse" aria-labelledby="flush-headingTwo" data-bs-parent="#qa-accordion">
                        <p class="
                                accordion-body
                                mb-0
                                pe-3
                                fs-sm
                                lh-lg
                                text-secondary
                              ">
                          提供產品售後服務，對產品本體(不含配件、線材)提供二年保固服務。產品因意外或人為不當使用或未經授權維修等非依使用手冊使用而造成產品損壞者，則不在保固範圍之內，得向客戶酌收產品維修服務費用。
                        </p>
                      </div>
                    </li>
                    <li class="accordion-item">
                      <h2 class="accordion-header" id="flush-headingThree">
                        <button class="accordion-button btn-outline-warning collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#flush-collapseThree" aria-expanded="false" aria-controls="flush-collapseThree">
                          <span class="
                                  bg-warning
                                  text-dark
                                  font-baloo-tamma
                                  fw-bolder
                                  text-center
                                  rounded
                                  fs-sm
                                  me-3
                                  pt-1
                                  lh-lg
                                  letter-spacing-7
                                  px-2
                                ">
                            Q3
                          </span>
                          補充包底片要去哪裡購買呢？
                        </button>
                      </h2>
                      <div id="flush-collapseThree" class="accordion-collapse collapse" aria-labelledby="flush-headingThree" data-bs-parent="#qa-accordion">
                        <p class="
                                accordion-body
                                mb-0
                                pe-3
                                fs-sm
                                lh-lg
                                text-secondary
                              ">
                          本產品可以兼容 i-type 及 600
                          相片，各大網路平台皆有販售。
                        </p>
                      </div>
                    </li>
                    <li class="accordion-item">
                      <h2 class="accordion-header" id="flush-headingFour">
                        <button class="accordion-button btn-outline-warning collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#flush-collapseFour" aria-expanded="false" aria-controls="flush-collapseFour">
                          <span class="
                                  bg-warning
                                  text-dark
                                  font-baloo-tamma
                                  fw-bolder
                                  text-center
                                  rounded
                                  fs-sm
                                  me-3
                                  pt-1
                                  lh-lg
                                  letter-spacing-7
                                  px-2
                                ">
                            Q4
                          </span>
                          印出來的拍立得照片需要充電嗎？
                        </button>
                      </h2>
                      <div id="flush-collapseFour" class="accordion-collapse collapse" aria-labelledby="flush-headingFour" data-bs-parent="#qa-accordion">
                        <p class="
                                accordion-body
                                mb-0
                                pe-3
                                fs-sm
                                lh-lg
                                text-secondary
                              ">
                          不用，取出後稍微搖晃，相片與空氣接觸數秒後便會產生圖像顏色。
                        </p>
                      </div>
                    </li>
                    <li class="accordion-item">
                      <h2 class="accordion-header" id="flush-headingFive">
                        <button class="accordion-button btn-outline-warning collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#flush-collapseFive" aria-expanded="false" aria-controls="flush-collapseFive">
                          <span class="
                                  bg-warning
                                  text-dark
                                  font-baloo-tamma
                                  fw-bolder
                                  text-center
                                  rounded
                                  fs-sm
                                  me-3
                                  pt-1
                                  lh-lg
                                  letter-spacing-7
                                  px-2
                                ">
                            Q5
                          </span>
                          運送方式及付款方式有哪些呢？
                        </button>
                      </h2>
                      <div id="flush-collapseFive" class="accordion-collapse collapse" aria-labelledby="flush-headingFive" data-bs-parent="#qa-accordion">
                        <p class="
                                accordion-body
                                mb-0
                                pe-3
                                fs-sm
                                lh-lg
                                text-secondary
                              ">
                          可以選擇超商取貨及宅配，付款方式有銀行轉帳及信用卡支付。
                        </p>
                      </div>
                    </li>
                    <li class="accordion-item">
                      <h2 class="accordion-header" id="flush-headingSix">
                        <button class="accordion-button btn-outline-warning collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#flush-collapseSix" aria-expanded="false" aria-controls="flush-collapseSix">
                          <span class="
                                  bg-warning
                                  text-dark
                                  font-baloo-tamma
                                  fw-bolder
                                  text-center
                                  rounded
                                  fs-sm
                                  me-3
                                  pt-1
                                  lh-lg
                                  letter-spacing-7
                                  px-2
                                ">
                            Q6
                          </span>
                          退換貨方式及規則
                        </button>
                      </h2>
                      <div id="flush-collapseSix" class="accordion-collapse collapse" aria-labelledby="flush-headingSix" data-bs-parent="#qa-accordion">
                        <p class="
                                accordion-body
                                mb-0
                                pe-3
                                fs-sm
                                lh-lg
                                text-secondary
                              ">
                          因商品封條多為一次性包裝，商品退貨時必須回復原狀，亦即必須回復至您收到商品時的原始狀態，且會視回收的商品狀態另外酌收額外的整新費用，請您務必確認有購買需求後再行拆封，感謝您的配合。
                        </p>
                      </div>
                    </li>



                  </ul>

                </div>
                <!-- 目前進度 -->
                <div class="tab-pane fade" id="tab-qa" role="tabpanel"><ul class="list-unstyled">
              <li class="card mb-3">
                <div class="row g-0">
                  <div class="col-auto">
                    <img src="https://ecjia.com.tw/demo/bs5_homework_0526/assets/news01.jpg" alt="消息示意圖" class="news-img d-lg-none d-xl-block" />
                  </div>
                  <div class="col">
                    <div class="card-body">
                      <h4 class="card-title fs-6 fw-bold mb-0">
                        高雄體驗會｜免費參加送帆布袋
                      </h4>
                      <small class="
                              text-secondary
                              my-2
                              font-baloo-tamma
                              d-block
                              w-100
                              fw-normal
                            ">2021-6-20</small>
                      <p class="
                              card-text
                              text-secondary
                              fs-sm
                              d-none d-md-block
                              pb-3
                            ">
                        大家安安！謝謝每位贊助者的熱情支持，讓我們離夢想更進一步，我們將於下個月舉辦體驗會，歡迎各位踴躍參與！
                      </p>
                      <a href="#" class="
                              link-danger
                              font-baloo-tamma
                              fw-bold
                              pb-2
                              fs-6
                              position-absolute
                              bottom-0
                            ">MORE</a>
                    </div>
                  </div>
                </div>
              </li>
              <li class="card mb-3">
                <div class="row g-0">
                  <div class="col-auto">
                    <img src="https://ecjia.com.tw/demo/bs5_homework_0526/assets/news02.jpg" alt="消息示意圖" class="news-img d-lg-none d-xl-block" />
                  </div>
                  <div class="col">
                    <div class="card-body">
                      <h4 class="card-title fw-bold fs-6 mb-0">
                        高雄體驗會｜免費參加送帆布袋
                      </h4>
                      <small class="
                              text-secondary
                              my-2
                              font-baloo-tamma
                              d-block
                              w-100
                              fw-normal
                            ">2021-6-20</small>
                      <p class="
                              card-text
                              text-secondary
                              fs-sm
                              d-none d-md-block
                              pb-3
                            ">
                        大家安安！謝謝每位贊助者的熱情支持，讓我們離夢想更進一步，我們將於下個月舉辦體驗會，歡迎各位踴躍參與！
                      </p>
                      <a href="#" class="
                              link-danger
                              font-baloo-tamma
                              fw-bold
                              pb-2
                              fs-6
                              position-absolute
                              bottom-0
                            ">MORE</a>
                    </div>
                  </div>
                </div>
              </li>
              <li class="card mb-3">
                <div class="row g-0">
                  <div class="col-auto">
                    <img src="https://ecjia.com.tw/demo/bs5_homework_0526/assets/news03.jpg" alt="消息示意圖" class="news-img d-lg-none d-xl-block" />
                  </div>
                  <div class="col">
                    <div class="card-body">
                      <h4 class="card-title fs-6 fw-bold mb-0">
                        高雄體驗會｜免費參加送帆布袋
                      </h4>
                      <small class="
                              text-secondary
                              my-2
                              font-baloo-tamma
                              d-block
                              w-100
                              fw-normal
                            ">2021-6-20</small>
                      <p class="
                              card-text
                              text-secondary
                              fs-sm
                              d-none d-md-block
                              pb-3
                            ">
                        大家安安！謝謝每位贊助者的熱情支持，讓我們離夢想更進一步，我們將於下個月舉辦體驗會，歡迎各位踴躍參與！
                      </p>
                      <a href="#" class="
                              link-danger
                              font-baloo-tamma
                              fw-bold
                              pb-2
                              fs-6
                              position-absolute
                              bottom-0
                            ">MORE</a>
                    </div>
                  </div>
                </div>
              </li>
            </ul>
            </div>
                <!-- 留言 -->
                <div class="tab-pane fade" id="tab-comment" role="tabpanel">
                  <div class="
                    border-3
                    rounded
                    border-start border-warning
                    p-3
                    text-dark
                    mb-3
                    d-none d-md-block
                    letter-spacing-7
                    bg-gray-100
                  ">
              只有本專案的贊助者才可以留言哦，如果有任何專案相關的問題，歡迎<a href="#" class="link-danger">聯絡提案人</a>！
            </div>
            <ul class="mb-4 list-unstyled">
              <li class="mb-3">
                <div class="border rounded-4 p-3 comment">
                  <div class="d-flex justify-content-start">
                    <img src="https://ecjia.com.tw/demo/bs5_homework_0526/assets/user_img01.jpg" alt="廖小杰個人頭像" />
                    <div class="d-flex flex-column align-items-start ms-3">
                      <a href="#" class="
                              letter-spacing-20
                              fs-5 fs-5-rfs
                              link-gray-700
                            " style="text-decoration:none;">
                        廖小杰
                      </a>
                      <small class="text-secondary fs-sm letter-spacing-20">
                        2020年5月22日 11:32
                      </small>
                    </div>
                  </div>
                  <p class="text-gray-800 my-3 letter-spacing-7">
                    晚上起床上廁所看到照片裡的人一直動其實有點恐怖，希望可以有暫停或是定時的功能！
                  </p>
                  <div class="
                          text-gray-800
                          p-3
                          bg-light
                          rounded-2
                          letter-spacing-7
                        ">
                    <span class="
                            text-danger
                            w-100
                            fs-sm
                            d-block
                            mb-2
                            letter-spacing-6
                          ">提案者回覆</span>
                    你要嘛起床的時候開燈，要嘛給我們更多錢開發阿
                  </div>
                </div>
              </li>
              <li class="mb-3">
                <div class="border rounded-4 p-3 comment">
                  <div class="d-flex justify-content-start">
                    <img src="https://ecjia.com.tw/demo/bs5_homework_0526/assets/user_img02.jpg" alt="卡阿伯個人頭像" />
                    <div class="d-flex flex-column align-items-start ms-3">
                      <a href="#" class="letter-spacing-20 fs-5 link-gray-700" style="text-decoration:none;">卡阿伯</a>
                      <small class="text-secondary fs-sm letter-spacing-20">2020年5月22日 11:32</small>
                    </div>
                  </div>
                  <p class="text-gray-800 my-3 letter-spacing-7">
                    希望有更多花色可以選擇！我女兒最近喜歡綠色
                  </p>
                </div>
              </li>
              <li class="mb-3">
                <div class="border rounded-4 p-3 comment">
                  <div class="d-flex justify-content-start">
                    <img src="https://ecjia.com.tw/demo/bs5_homework_0526/assets/user_img02.jpg" alt="賈師個人頭像" />
                    <div class="d-flex flex-column align-items-start ms-3">
                      <a href="#" class="fs-5 link-gray-700 letter-spacing-20" style="text-decoration:none;">賈師</a>
                      <small class="text-secondary fs-sm letter-spacing-20">2020年5月22日 11:32</small>
                    </div>
                  </div>
                  <p class="text-gray-800 my-3 letter-spacing-7">
                    可以做個相簿功能嗎？拍出好看的影片再讓我們選擇要印出哪一張這樣
                  </p>
                </div>
              </li>
              <li>
                <div class="border rounded-4 p-3 comment">
                  <div class="d-flex justify-content-start">
                    <img src="https://ecjia.com.tw/demo/bs5_homework_0526/assets/user_img02.jpg" alt="俊俊個人頭像" />
                    <div class="d-flex flex-column align-items-start ms-3">
                      <a href="#" class="fs-5 link-gray-700 letter-spacing-20" style="text-decoration:none;">俊俊</a>
                      <small class="text-secondary fs-sm letter-spacing-20">2020年5月22日 11:32</small>
                    </div>
                  </div>
                  <p class="text-gray-800 my-3">
                    test123 看一下我是不是真的可以留言
                  </p>
                </div>
              </li>
            </ul>



                </div>
              </div>
            <!-- 手機版逼人贊助卡片區塊 -->
            <div class="mb-5 d-lg-none">
            <div class="border rounded-4 p-3">
                <div class="d-flex justify-content-start align-items-center">
                <img src="https://ecjia.com.tw/demo/bs5_homework_0526/assets/store_img.jpg" class="rounded-pill border-2 border-warning border" alt="缺錢事務所" />
                <div class="ps-3">
                    <h4 class="fs-5">缺錢事務所</h4>
                    <p class="text-gray-800 letter-spacing-7">
                    已發起 <strong>1</strong> 個專案
                    </p>
                </div>
                </div>
                <p class="my-3 fs-6">
                需要點錢錢做些酷酷的東西，拜託各位乾爹乾媽囉！
                </p>
                <div class="d-flex justify-content-between align-items-center">
                <div class="d-flex">
                    <a href="#" class="
                            btn-secondary btn-warning-hover
                            rounded-circle
                            text-center
                            me-2
                            card-icon
                        ">
                    <i class="fab fa-facebook-f text-white"></i>
                    </a>
                    <a href="#" class="
                            btn-secondary btn-warning-hover
                            rounded-circle
                            text-center
                            card-icon
                        ">
                    <i class="fab fa-youtube text-white"></i>
                    </a>
                </div>
                <button class="
                        btn
                        btn-sm
                        btn-outline-secondary
                        btn-outline-secondary-hover
                        rounded-pill
                        px-3
                        ">
                    <i class="far fa-comment-dots me-2 text-secondary"></i>聯絡我們
                </button>
                </div>
            </div>
            <h3 class="
                    mt-4
                    bg-light
                    border-start border-end border-4 border-warning
                    fw-bold
                    text-center
                    p-2
                    rounded
                    fs-5
                    letter-spacing-20
                    ">
                選擇一個方案來支持
            </h3>
            <div class="card mt-3">
                <img src="https://ecjia.com.tw/demo/bs5_homework_0526/assets/img.jpg" class="card-img-top" alt="廣告/團購優惠" />
                <div class="card-body pt-2">
                <div class="
                        d-flex
                        justify-content-between
                        align-items-center
                        border-bottom
                        pb-1
                        mb-3
                        ">
                    <span class="text-dark fs-sm">限時優惠</span>
                    <span class="font-baloo-tamma text-dark fs-sm">2 days 20:05:20</span>
                </div>
                <h3 class="letter-spacing-20 fw-bold fs-5">
                    買一送一，只有兩百組別錯過
                </h3>
                <p class="font-baloo-tamma fw-bolder fs-4 mb-0">NT$ 1600</p>
                <span class="badge bg-gray-200 text-secondary px-3 me-1">已被贊助88次</span>
                <span class="badge bg-secondary text-white px-3">限量<span class="text-warning">200</span>個</span>
                <p class="letter-spacing-7 text-justify text-secondary mt-2">
                    受就相法大夠局來畫師我只這然以放灣得的後人心年我物我年，或人有動與次出女親構算帶年行著所間女。
                </p>
                <a href="#" class="
                        btn btn-warning btn-warning-hover
                        rounded-pill
                        w-100
                        fw-bold
                        ">贊助此專案</a>
                </div>
            </div>
            <div class="card mt-3">
                <img src="https://ecjia.com.tw/demo/bs5_homework_0526/assets/img.jpg" class="card-img-top" alt="廣告/團購優惠" />
                <div class="card-body pt-2">
                <div class="
                        d-flex
                        justify-content-between
                        align-items-center
                        border-bottom
                        pb-1
                        mb-3
                        ">
                    <span class="text-dark fs-sm">限時優惠</span>
                    <span class="font-baloo-tamma text-dark fs-sm">2 days 20:05:20</span>
                </div>
                <h3 class="letter-spacing-20 fw-bold fs-5">
                    買一送一，只有兩百組別錯過
                </h3>
                <p class="font-baloo-tamma fw-bolder fs-4 mb-0">NT$ 1600</p>
                <span class="badge bg-gray-200 text-secondary px-3 me-1">已被贊助88次</span>
                <span class="badge bg-secondary text-white px-3">限量<span class="text-warning">200</span>個</span>
                <p class="letter-spacing-7 text-justify text-secondary mt-2">
                    受就相法大夠局來畫師我只這然以放灣得的後人心年我物我年，或人有動與次出女親構算帶年行著所間女。
                </p>
                <a href="#" class="
                        btn btn-warning btn-warning-hover
                        rounded-pill
                        w-100
                        fw-bold
                        ">贊助此專案</a>
                </div>
            </div>
            <div class="card mt-3">
                <img src="https://ecjia.com.tw/demo/bs5_homework_0526/assets/img.jpg" class="card-img-top" alt="廣告/團購優惠" />
                <div class="card-body pt-2">
                <div class="
                        d-flex
                        justify-content-between
                        align-items-center
                        border-bottom
                        pb-1
                        mb-3
                        ">
                    <span class="text-dark fs-sm">限時優惠</span>
                    <span class="font-baloo-tamma text-dark fs-sm">2 days 20:05:20</span>
                </div>
                <h3 class="letter-spacing-20 fw-bold fs-5">
                    買一送一，只有兩百組別錯過
                </h3>
                <p class="font-baloo-tamma fw-bolder fs-4 mb-0">NT$ 1600</p>
                <span class="badge bg-gray-200 text-secondary px-3 me-1">已被贊助88次</span>
                <span class="badge bg-secondary text-white px-3">限量<span class="text-warning">200</span>個</span>
                <p class="letter-spacing-7 text-justify text-secondary mt-2">
                    受就相法大夠局來畫師我只這然以放灣得的後人心年我物我年，或人有動與次出女親構算帶年行著所間女。
                </p>
                <a href="#" class="
                        btn btn-warning btn-warning-hover
                        rounded-pill
                        w-100
                        fw-bold
                        ">贊助此專案</a>
                </div>
            </div>
            </div>


              <!-- 募資表單 -->
              <!-- <h2 id="sponsor">我要贊助</h2> -->
              <div class="d-flex justify-content-center">
                <img src="https://ecjia.com.tw/demo/bs5_homework_0526/assets/hezuo.svg" alt="合作圖標" />
              </div>
              <div class="position-relative my-4">
                <div class="progress bg-warning" style="height: 3px">
                  <div class="progress-bar" role="progressbar" aria-valuenow="0" aria-valuemin="0" aria-valuemax="100"></div>
                </div>
                <h2 class="position-absolute top-0 start-50 translate-middle bg-white text-center px-3 fs-3 fw-bold ">
                  贊助專案
                </h2>
              </div>  


              <form id="form" class="needs-validation" @submit="checkForm" novalidate>
                <div class="mb-3">
                  <label for="project" class="form-label">贊助方案</label>
                  <select class="form-select form-sponsor" id="project" aria-label="select project" required>
                    <option value="" selected="selected">請選擇一個方案</option>
                    <option value="1">方案1</option>
                    <option value="2">方案2</option>
                    <option value="3">方案3</option>
                  </select>
                  <div class="invalid-feedback">請選擇一個方案</div>
                </div>

                <div class="mb-3">
                  <label for="name" class="form-label">收件人姓名</label>
                  <input type="text" class="form-control form-sponsor" id="name" required />
                  <div class="invalid-feedback">請輸入正確的收件人姓名</div>
                </div>

                <div class="mb-3">
                  <label for="address" class="form-label">收件地址</label>
                  <input type="text" class="form-control form-sponsor" id="address" required />
                  <div class="invalid-feedback">請輸入正確的收件地址</div>
                </div>

                <div class="mb-3">
                  <label for="phone" class="form-label">聯絡電話</label>
                  <input type="text" class="form-control form-sponsor" id="phone" required />
                  <div class="invalid-feedback">請輸入正確的電話號碼</div>
                </div>

                <div class="mb-3">
                  <label for="email" class="form-label">聯絡信箱</label>
                  <input type="text" class="form-control form-sponsor" id="email" required />
                  <div class="invalid-feedback">請輸入正確的郵件格式</div>
                </div>
                <div class="mb-3">
                  <label for="payment" class="form-label">付款方式</label>
                  <select id="payment" class="form-select form-sponsor" aria-label="select payment" required>
                    <option value="" selected="">請選擇一種付款方式</option>
                    <option value="1">信用卡付款</option>
                    <option value="2">貨到付款</option>
                  </select>
                  <div class="invalid-feedback">請選擇一種付款方式</div>
                </div>

                <button type="submit" class="border-3 btn btn-warning btn-lg  btn-warning-hover px-5 fw-bold rounded-pill mt-2 w-100 d-md-none">贊助專案1</button>
                <div class="d-none d-md-flex justify-content-center border-3">
                  <button type="submit" class="border btn btn-warning btn-lg  px-5 fw-bold rounded-pill mt-2 btn-warning-hover" >贊助專案2
                  </button>
                </div>
              </form>
            </div>

            
<!-- 右邊 card 區塊 -->
      <div class="col-xxl-3 col-lg-4 d-none d-lg-block">
        <div class="position-sticky overflow-scroll top-nav h-100vh-nav">
          <div class="border rounded-4 p-3 mb-2">
            <div class="d-flex justify-content-start align-items-center">
              <img src="https://ecjia.com.tw/demo/bs5_homework_0526/assets/store_img.jpg" class="rounded-pill border-2 border-warning border" alt="缺錢事務所" />
              <div class="ps-3">
                <h4 class="letter-spacing-20 fs-5">缺錢事務所</h4>
                <p class="text-gray-800 letter-spacing-7">
                  已發起 <strong>1</strong> 個專案
                </p>
              </div>
            </div>
            <p class="my-3 fs-6 letter-spacing-7">
              需要點錢錢做些酷酷的東西，拜託各位乾爹乾媽囉！
            </p>
            <div class="d-flex justify-content-between align-items-center">
              <div class="d-flex">
                <a class="
                        btn-secondary btn-warning-hover
                        rounded-circle
                        text-center
                        me-2
                        card-icon
                      " href="#">
                  <i class="fab fa-facebook-f text-white"></i>
                </a>
                <a class="
                        btn-secondary btn-warning-hover
                        rounded-circle
                        text-center
                        card-icon
                      " href="#">
                  <i class="fab fa-youtube text-white"></i>
                </a>
              </div>
              <button class="
                      btn
                      btn-sm
                      btn-outline-secondary
                      btn-outline-secondary-hover
                      rounded-pill
                      px-3
                    ">
                <i class="far fa-comment-dots me-2 text-secondary"></i>聯絡我們
              </button>
            </div>
          </div>
          <h3 class="
                  mt-4
                  bg-light
                  border-start border-end border-4 border-warning
                  fw-bold
                  text-center
                  p-2
                  rounded
                  fs-5
                  letter-spacing-20
                ">
            選擇一個方案來支持
          </h3>
          <div class="card mt-3">
            <img src="https://ecjia.com.tw/demo/bs5_homework_0526/assets/img.jpg" class="card-img-top" alt="廣告/團購優惠" />
            <div class="card-body pt-2">
              <div class="
                      d-flex
                      justify-content-between
                      align-items-center
                      border-bottom
                      pb-1
                      mb-3
                    ">
                <span class="text-dark fs-sm">限時優惠</span>
                <span class="font-baloo-tamma text-dark fs-sm">2 days 20:05:20</span>
              </div>
              <h3 class="letter-spacing-20 fw-bold fs-5">
                買一送一，只有兩百組別錯過
              </h3>
              <p class="font-baloo-tamma fw-bolder fs-4 mb-0">NT$ 1600</p>
              <span class="badge bg-gray-200 text-secondary px-3">已被贊助88次</span>
              <span class="badge bg-secondary text-white px-3">限量<span class="text-warning">200</span>個</span>
              <p class="letter-spacing-7 text-justify text-secondary mt-2">
                受就相法大夠局來畫師我只這然以放灣得的後人心年我物我年，或人有動與次出女親構算帶年行著所間女。
              </p>
              <a href="#" class="
                      btn btn-warning btn-warning-hover
                      rounded-pill
                      w-100
                      fw-bold
                    ">贊助此專案</a>
            </div>
          </div>
          <div class="card mt-3">
            <img src="https://ecjia.com.tw/demo/bs5_homework_0526/assets/img.jpg" class="card-img-top" alt="廣告/團購優惠" />
            <div class="card-body pt-2">
              <div class="
                      d-flex
                      justify-content-between
                      align-items-center
                      border-bottom
                      pb-1
                      mb-3
                    ">
                <span class="text-dark fs-sm">限時優惠</span>
                <span class="font-baloo-tamma text-dark fs-sm">2 days 20:05:20</span>
              </div>
              <h3 class="letter-spacing-20 fw-bold fs-5">
                買一送一，只有兩百組別錯過
              </h3>
              <p class="font-baloo-tamma fw-bolder fs-4 mb-0">NT$ 1600</p>
              <span class="badge bg-gray-200 text-secondary px-3">已被贊助88次</span>
              <span class="badge bg-secondary text-white px-3">限量<span class="text-warning">200</span>個</span>
              <p class="letter-spacing-7 text-justify text-secondary mt-2">
                受就相法大夠局來畫師我只這然以放灣得的後人心年我物我年，或人有動與次出女親構算帶年行著所間女。
              </p>
              <a href="#" class="
                      btn btn-warning btn-warning-hover
                      rounded-pill
                      w-100
                      fw-bold
                    ">贊助此專案</a>
            </div>
          </div>
          <div class="card mt-3">
            <img src="https://ecjia.com.tw/demo/bs5_homework_0526/assets/img.jpg" class="card-img-top" alt="廣告/團購優惠" />
            <div class="card-body pt-2">
              <div class="
                      d-flex
                      justify-content-between
                      align-items-center
                      border-bottom
                      pb-1
                      mb-3
                    ">
                <span class="text-dark fs-sm">限時優惠</span>
                <span class="font-baloo-tamma text-dark fs-sm">2 days 20:05:20</span>
              </div>
              <h3 class="letter-spacing-20 fw-bold fs-5">
                買一送一，只有兩百組別錯過
              </h3>
              <p class="font-baloo-tamma fw-bolder fs-4 mb-0">NT$ 1600</p>
              <span class="badge bg-gray-200 text-secondary px-3">已被贊助88次</span>
              <span class="badge bg-secondary text-white px-3">限量<span class="text-warning">200</span>個</span>
              <p class="letter-spacing-7 text-justify text-secondary mt-2">
                受就相法大夠局來畫師我只這然以放灣得的後人心年我物我年，或人有動與次出女親構算帶年行著所間女。
              </p>
              <a href="#" class="
                      btn btn-warning btn-warning-hover
                      rounded-pill
                      w-100
                      fw-bold
                    " id="oraginBtn">贊助此專案</a>
            </div>
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


</style>