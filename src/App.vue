<script setup>
import { onMounted, onUnmounted } from "vue";
import { RouterView } from "vue-router";

//example components
import NavbarDefault from "@/components/NavbarDefault.vue";
import FooterDefault from "@/components/FooterDefault.vue";

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
  <div class="container position-sticky z-index-sticky top-0">
    <div class="row">
      <div class="col-12">
        <NavbarDefault :sticky="true" />
      </div>
    </div>
  </div>
  <router-view />
  <FooterDefault />
</template>