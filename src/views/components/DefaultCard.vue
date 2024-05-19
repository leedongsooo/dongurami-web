<template>
  <div class="card mt-4">
    <div class="card-header pb-0 p-3">
      <div class="row">
        <div class="col-6 d-flex align-items-center">
          <h6 class="mb-0">수정할텐가</h6>
        </div>
        <div class="col-6 text-end">
          <vsud-button color="dark" variant="gradient">
            <i class="fas fa-plus me-2"></i>
            수정
          </vsud-button>
        </div>
      </div>
    </div>
    <div class="card-body p-3">
      <div class="row">
        <div class="col-md-6 mb-md-0 mb-4">
          <div
            class="card card-body border card-plain border-radius-lg d-flex align-items-center flex-row"
          >
            <h6 class="mb-0">하나둘삼넷</h6>
            <i
              class="fas fa-pencil-alt ms-auto text-dark cursor-pointer"
              data-bs-toggle="tooltip"
              data-bs-placement="top"
              title
              aria-hidden="true"
              data-bs-original-title="Edit Card"
              aria-label="Edit Card"
            ></i>
          </div>
        </div>

      </div>
    </div>
  </div>
</template>

<script>
import VsudButton from "@/components/VsudButton.vue";

export default {
  name: "DefaultCard",
  components: {
    VsudButton,
  },
};
</script>
