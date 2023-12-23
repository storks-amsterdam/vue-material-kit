<script setup>
import { onMounted, onUnmounted } from "vue";

//example components
import Header from "@/examples/Header.vue";

// sections
import BuiltByDevelopers from "@/views/Presentation/Components/BuiltByDevelopers.vue";
import PresentationTestimonials from "@/views/Presentation/Sections/PresentationTestimonials.vue";
import PresentationInformation from "@/views/Presentation/Sections/PresentationInformation.vue";

//images
import vueBLLHeader from "@/assets/img/dreamteam_burning.png";

//hooks
const body = document.getElementsByTagName("body")[0];
onMounted(() => {
  body.classList.add("presentation-page");
  body.classList.add("bg-gray-200");
});
onUnmounted(() => {
  body.classList.remove("presentation-page");
  body.classList.remove("bg-gray-200");
});
</script>

<template>
  <Header>
    <div
      class="page-header min-vh-75"
      :style="`background-image: url(${vueBLLHeader})`"
      loading="lazy"
    >
      <div class="container">
        <div class="row">
          <div class="col-lg-7 text-center mx-auto position-relative">
            <h1
              class="text-white pt-3 mt-n5 me-2"
              :style="{ display: 'inline-block ' }"
            >
              Burning Lowlands
            </h1>
            <p class="lead text-white px-5 mt-3" :style="{ fontWeight: '500' }">
              Wild fire prevention, preparadeness and regulatory environment in the Netherlands
            </p>
          </div>
        </div>
      </div>
    </div>
  </Header>

  <div class="card card-body blur shadow-blur mx-3 mx-md-4 mt-n6">
    <PresentationInformation />
    <BuiltByDevelopers />
    <PresentationTestimonials />
  </div>
</template>