<template>
  <div class="py-4 container-fluid">
    <div class="row">
      <div class="col-lg-7 mb-lg-0 mb-4">
        <div class="card">
          <div class="card-body p-3">
            <div class="row">
              <div class="col-lg-6">
                <div class="d-flex flex-column h-100">
                  <p class="mb-1 pt-2 text-bold">동아리 정보</p>
                  <h5 class="font-weight-bolder">FLAG</h5>
                  <p class="mb-3">
                    총 인원 수: 120 명
                  </p>
                  <p class="mb-2">
                    소속 분과: 정통, 컴학?
                  </p>
                </div>
              </div>
              <div class="col-lg-5 ms-auto text-center mt-5 mt-lg-0">
                <div class="bg-gradient-success border-radius-lg h-100">
                  <img
                    src="../assets/img/shapes/waves-white.svg"
                    class="position-absolute h-100 w-50 top-0 d-lg-block d-none"
                    alt="waves"
                  />
                  <div
                    class="position-relative d-flex align-items-center justify-content-center h-100"
                  >
                    <img
                      class="w-100 position-relative z-index-2 pt-4"
                      src="../assets/img/illustrations/rocket-white.png"
                      alt="rocket"
                    />
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="col-lg-5">
        <div class="card h-100 p-3">
          <div
            class="overflow-hidden position-relative border-radius-lg bg-cover h-100"
            style="
              background-image: url('https://demos.creative-tim.com/soft-ui-dashboard/assets/img/ivancik.jpg');
            "
          >
            <span class="mask bg-gradient-dark"></span>
            <div
              class="card-body position-relative z-index-1 d-flex flex-column h-100 p-3"
            >
              <h5 class="text-white font-weight-bolder mb-4 pt-2">
                동아리 프로필 수정
              </h5>
              <p class="text-white">
                동아리 메인프로필 사진 수정하기
              </p>
              <a
                class="text-white text-sm font-weight-bold mb-0 icon-move-right mt-auto"
                href="javascript:;"
              >
                CLICK
                <i
                  class="fas fa-arrow-right text-sm ms-1"
                  aria-hidden="true"
                ></i>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="row my-4">
      <div class="col-lg-12 col-md-6 mb-md-0 mb-4">
        <projects-card />
      </div>
    </div>
  </div>
</template>
<script>

import ProjectsCard from "./components/ProjectsCard.vue";

export default {
  name: "DashboardDefault",
  components: {
    ProjectsCard,
  },

};
</script>
