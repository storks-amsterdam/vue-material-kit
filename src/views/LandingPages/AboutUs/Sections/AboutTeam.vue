<script setup>
// example component
import HorizontalTeamCard from "@/examples/cards/teamCards/HorizontalTeamCard.vue";

// images
import urte from "@/assets/img/team/urte.jpg";
import janneke from "@/assets/img/team/janneke.jpg";
import rishika from "@/assets/img/team/rishika.jpg";
import reggie from "@/assets/img/team/reggie.jpg";
import aleksey from "@/assets/img/team/aleksey.jpg";
import iokasti from "@/assets/img/team/iokasti.jpg";
import marko from "@/assets/img/team/marko.jpg";
import saar from "@/assets/img/team/saar.jpg";
import sarah from "@/assets/img/team/sarah.jpg";
// import shiaar from "@/assets/img/team/shiaar.jpg";
// import heloise from "@/assets/img/team/heloise.jpg";
import thomas from "@/assets/img/team/thomas.jpg";
</script>

<template>
  <section class="pb-5 position-relative mx-n3">
    <div class="container">
      <div class="row">
        <div class="col-md-8 text-start mb-5 mt-5">
          <h3 class="text-dark z-index-1 position-relative">
            The Research Team
          </h3>
          <p class="text-dark opacity-8 mb-0">
            We are all current or former VU students.
          </p>
        </div>
      </div>
      <div class="row">
        <div class="col-lg-6 col-12">
          <HorizontalTeamCard
            class="mt-lg-4 mt-5"
            :image="janneke"
            :profile="{ name: 'Janneke Parrish', link: 'javascript:;' }"
            :position="{ label: 'Project Manager', color: 'success' }"
            description="LLB: Law in Society"
          />
        </div>
        <div class="col-lg-6 col-12">
          <HorizontalTeamCard
            class="mt-4"
            :image="urte"
            :profile="{ name: 'Urtė Drabataitė', link: 'javascript:;' }"
            :position="{ label: 'PPE Team', color: 'success' }"
            description="Environment and Resource Management"
          />
        </div>
      </div>
      <div class="row mt-4">
        <div class="col-lg-6 col-12">
          <HorizontalTeamCard
            class="mt-lg-4 mt-5"
            :image="rishika"
            :profile="{ name: 'Rishika Goswami', link: 'javascript:;' }"
            :position="{ label: 'PPE Team', color: 'success' }"
            description="Biomedical Sciences"
          />
        </div>
        <div class="col-lg-6 col-12">
          <HorizontalTeamCard
            class="mt-4"
            :image="reggie"
            :profile="{ name: 'Reggie Karssiens', link: 'javascript:;' }"
            :position="{ label: 'Vegetation Team', color: 'success' }"
            description="Aarde, Economie en Duurzaamheid"
          />
        </div>
      </div>
      <div class="row mt-4">
        <div class="col-lg-6 col-12">
          <HorizontalTeamCard
            class="mt-lg-4 mt-5"
            :image="aleksey"
            :profile="{ name: 'Aleksey Martynyuk', link: 'javascript:;' }"
            :position="{ label: 'Vegetation team / IT', color: 'success' }"
            description="Artificial Intelligence"
          />
        </div>
        <div class="col-lg-6 col-12">
          <HorizontalTeamCard
            class="mt-4"
            :image="iokasti"
            :profile="{ name: 'Iokasti Perganta', link: 'javascript:;' }"
            :position="{ label: 'Vegetation Team', color: 'success' }"
            description="Biomedical Sciences"
          />
        </div>
      </div>
      <div class="row mt-4">
        <div class="col-lg-6 col-12">
          <HorizontalTeamCard
            class="mt-lg-4 mt-5"
            :image="marko"
            :profile="{ name: 'Marko Daraboš', link: 'javascript:;' }"
            :position="{ label: 'Policy Team', color: 'success' }"
            description="International Business Administration"
          />
        </div>
        <div class="col-lg-6 col-12">
          <HorizontalTeamCard
            class="mt-4"
            :image="saar"
            :profile="{ name: 'Saar Van Der Kolk', link: 'javascript:;' }"
            :position="{ label: 'Vegetation Team', color: 'success' }"
            description="Aarde, Economie en Duurzaamheid"
          />
        </div>
      </div>
      <div class="row mt-4">
        <div class="col-lg-6 col-12">
          <HorizontalTeamCard
            class="mt-lg-4 mt-5"
            :image="sarah"
            :profile="{ name: 'Sarah Foster', link: 'javascript:;' }"
            :position="{ label: 'Policy Team', color: 'success' }"
            description="Environmental Humanities"
          />
        </div>
        <div class="col-lg-6 col-12">
          <HorizontalTeamCard
            class="mt-4"
            :image="thomas"
            :profile="{ name: 'dr. ir. Thomas Janssen', link: 'javascript:;' }"
            :position="{ label: 'Ambassador', color: 'success' }"
            description="Postdoctoral researcher at the Climate and Ecosystem Change group"
          />
        </div>
      </div>
    </div>
  </section>
</template>
