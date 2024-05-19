<template>
  <div class="nav-wrapper position-relative end-0">
    <ul class="nav nav-pills nav-fill p-1" role="tablist">
      <li class="nav-item">
        <a
          class="nav-link mb-0 px-0 py-1 active active"
          data-bs-toggle="tab"
          href="../../../examples/pages/account/settings.html"
          role="tab"
          aria-selected="true"
          >버튼 하나</a
        >
      </li>
      <li class="nav-item">
        <a
          class="nav-link mb-0 px-0 py-1"
          data-bs-toggle="tab"
          href="../../../examples/pages/account/billing.html"
          role="tab"
          aria-selected="false"
          >버튼 둘</a
        >
      </li>
      <li class="nav-item">
        <a
          class="nav-link mb-0 px-0 py-1"
          data-bs-toggle="tab"
          href="../../../examples/pages/account/invoice.html"
          role="tab"
          aria-selected="false"
          >버튼 삼</a
        >
      </li>
      <li class="nav-item">
        <a
          class="nav-link mb-0 px-0 py-1"
          data-bs-toggle="tab"
          href="../../../examples/pages/account/security.html"
          role="tab"
          aria-selected="false"
          >버튼 넷</a
        >
      </li>
    </ul>
  </div>
</template>

<script>
import setNavPills from "@/assets/js/nav-pills.js";

export default {
  name: "NavPill",
  mounted() {
    setNavPills();
  },
};
</script>
