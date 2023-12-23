<script setup>
import { onMounted, onUnmounted } from "vue";

//example components
import LeafletMap from "@/components/LeafletMap.vue";

//image
import bg0 from "@/assets/img/earth-from-space-europe.jpg";

//dep
import Typed from "typed.js";

const body = document.getElementsByTagName("body")[0];
//hooks
onMounted(() => {
  body.classList.add("about-us");
  body.classList.add("bg-gray-200");

  if (document.getElementById("typed")) {
    // eslint-disable-next-line no-unused-vars
    var typed = new Typed("#typed", {
      stringsElement: "#typed-strings",
      typeSpeed: 90,
      backSpeed: 90,
      backDelay: 200,
      startDelay: 500,
      loop: true,
    });
  }
});

onUnmounted(() => {
  body.classList.remove("about-us");
  body.classList.remove("bg-gray-200");
});
</script>
<template>
  <header class="bg-gradient-dark">
    <div
      class="page-header min-vh-50"
      :style="{ backgroundImage: `url(${bg0})` }"
    >
      <span class="mask bg-gradient-dark opacity-6"></span>
      <div class="container">
        <div class="row justify-content-center">
          <div class="col-lg-8 text-center mx-auto my-auto">
            <h1 class="text-white">
              We provide <span class="text-white" id="typed"></span>
            </h1>
            <div id="typed-strings">
              <h1>data</h1>
              <h1>analysis</h1>
              <h1>maps</h1>
            </div>
            <p class="lead mb-4 text-white opacity-8">
              High resolutuion open source data from Copernicus data platform
            </p>
            <a href="https://dataspace.copernicus.eu/" target="_blank">
              <button type="submit" class="btn bg-white text-dark">
                Copernicus Data Space
              </button>
            </a>
          </div>
        </div>
      </div>
    </div>
  </header>
  <div class="card card-body bg-gradient-dark shadow-xl mx-3 mx-md-4 mt-n6">
    <section class="pb-5 position-relative bg-gradient-dark mx-n3">
      <div class="container">
        <div class="row">
          <div class="col-lg-7 text-center mx-auto position-relative">
            <LeafletMap></LeafletMap>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>
