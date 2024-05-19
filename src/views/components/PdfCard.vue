<template>
  <div class="card h-100 mt-4">
    <div class="card-header pb-0 p-3">
      <div class="row">
        <div class="col-6 d-flex align-items-center">
          <h6 class="mb-0">동아리 자료</h6>
        </div>
        <div class="col-6 text-end">
          <vsud-button color="success" size="sm" variant="outline">모두 보기</vsud-button>
        </div>
      </div>
    </div>
    <div class="card-body p-3 pb-0 mb-0">
      <ul class="list-group">
        <li
          class="list-group-item border-0 d-flex justify-content-between ps-0 mb-2 border-radius-lg"
        >
          <div class="d-flex flex-column">
            <h6 class="mb-1 text-dark font-weight-bold text-sm">소개 자료</h6>
            <span class="text-xs">#1</span>
          </div>
          <div class="d-flex align-items-center text-sm">
            전체공개
            <button class="btn btn-link text-dark text-sm mb-0 px-0 ms-4">
              <i class="fas fa-file-pdf text-lg me-1" aria-hidden="true"></i> PDF
            </button>
          </div>
        </li>

        <li
            class="list-group-item border-0 d-flex justify-content-between ps-0 mb-2 border-radius-lg"
        >
          <div class="d-flex flex-column">
            <h6 class="mb-1 text-dark font-weight-bold text-sm">소개 자료</h6>
            <span class="text-xs">#1</span>
          </div>
          <div class="d-flex align-items-center text-sm">
            전체공개
            <button class="btn btn-link text-dark text-sm mb-0 px-0 ms-4">
              <i class="fas fa-file-pdf text-lg me-1" aria-hidden="true"></i> PDF
            </button>
          </div>
        </li>

        <li
            class="list-group-item border-0 d-flex justify-content-between ps-0 mb-2 border-radius-lg"
        >
          <div class="d-flex flex-column">
            <h6 class="mb-1 text-dark font-weight-bold text-sm">소개 자료</h6>
            <span class="text-xs">#1</span>
          </div>
          <div class="d-flex align-items-center text-sm">
            전체공개
            <button class="btn btn-link text-dark text-sm mb-0 px-0 ms-4">
              <i class="fas fa-file-pdf text-lg me-1" aria-hidden="true"></i> PDF
            </button>
          </div>
        </li>

        <li
            class="list-group-item border-0 d-flex justify-content-between ps-0 mb-2 border-radius-lg"
        >
          <div class="d-flex flex-column">
            <h6 class="mb-1 text-dark font-weight-bold text-sm">소개 자료</h6>
            <span class="text-xs">#1</span>
          </div>
          <div class="d-flex align-items-center text-sm">
            전체공개
            <button class="btn btn-link text-dark text-sm mb-0 px-0 ms-4">
              <i class="fas fa-file-pdf text-lg me-1" aria-hidden="true"></i> PDF
            </button>
          </div>
        </li>

        <li
            class="list-group-item border-0 d-flex justify-content-between ps-0 mb-2 border-radius-lg"
        >
          <div class="d-flex flex-column">
            <h6 class="mb-1 text-dark font-weight-bold text-sm">소개 자료</h6>
            <span class="text-xs">#1</span>
          </div>
          <div class="d-flex align-items-center text-sm">
            전체공개
            <button class="btn btn-link text-dark text-sm mb-0 px-0 ms-4">
              <i class="fas fa-file-pdf text-lg me-1" aria-hidden="true"></i> PDF
            </button>
          </div>
        </li>

        <li
            class="list-group-item border-0 d-flex justify-content-between ps-0 mb-2 border-radius-lg"
        >
          <div class="d-flex flex-column">
            <h6 class="mb-1 text-dark font-weight-bold text-sm">소개 자료</h6>
            <span class="text-xs">#1</span>
          </div>
          <div class="d-flex align-items-center text-sm">
            전체공개
            <button class="btn btn-link text-dark text-sm mb-0 px-0 ms-4">
              <i class="fas fa-file-pdf text-lg me-1" aria-hidden="true"></i> PDF
            </button>
          </div>
        </li>

      </ul>
    </div>
  </div>
</template>

<script>
import VsudButton from "@/components/VsudButton.vue";

export default {
  name: "PdfCard",
  components: {
    VsudButton,
  },
};
</script>
