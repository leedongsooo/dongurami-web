<template>
  <div class="container-fluid mt-4">
    <div class="row align-items-center">
      <div class="col-lg-4 col-sm-8">
        <nav-pill />
      </div>
    </div>
    <div class="row">
      <div class="col-lg-8">
        <div class="row mt-4">
          <div class="col-xl-6">
            <div class="row">

              <div class="col-md-6">
                <default-info-card
                  :class-icon="gibon.classIcon"
                  :title="gibon.title"
                  :desc="gibon.desc"
                  :price="gibon.price"
                />
              </div>
            </div>
          </div>
          <div class="col-md-12 mb-4">
            <default-card />
          </div>
        </div>
      </div>
      <div class="col-lg-4">
        <pdf-card />
      </div>
    </div>
    <div class="row mt-4">
      <div class="col-md-7">
        <information-card />
      </div>
      <div class="col-md-5 mt-4">
      </div>
    </div>
  </div>
</template>

<script>
import setTooltip from "@/assets/js/tooltip.js";
import NavPill from "./components/NavPill.vue";
import DefaultInfoCard from "@/examples/Cards/DefaultInfoCard.vue";
import DefaultCard from "./components/DefaultCard.vue";
import PdfCard from "./components/PdfCard.vue";
import InformationCard from "./components/InformationCard.vue";


export default {
  name: "IntroducePage",
  components: {
    NavPill,
    DefaultInfoCard,
    DefaultCard,
    PdfCard,
    InformationCard,
  },
  data() {
    return {
      gibon: {
        classIcon: "text-white fab fa-paypal",
        title: "예시",
        desc: "Payment",
        price: "123456",
      },
    };
  },
  mounted() {
    setTooltip();
  },
};
</script>
