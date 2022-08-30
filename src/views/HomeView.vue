<template>
  <div class="home flex w-full h-screen">
    <side-bar-component
      class="md:w-1/5 lg:w-1/6 bket-side-bar p-5 side-bar-w show-menu"
    />
    <div class="bket-home md:w-4/5 lg:w-5/6 side-bar-c p-7">
      <div
        class="bket-home-header flex w-full justify-between items-center h-16"
      >
        <div class="flex items-center w-30p">
          <div class="mr-3 flex flex-wrap">
            <label class="black-80 font-bold">Welcome back, </label>
            <label class="black-49 font-bold flex"
              >Francois AISSAN
              <img class="ml-2" src="../assets/images/wave.png"
            /></label>
          </div>
          <div></div>
        </div>
        <div class="w-40p">
          <div class="relative">
            <img
              class="absolute position-img w-4"
              src="../assets/images/Union.png"
            />
            <input
              class="search-input w-full p-53p"
              type="search"
              placeholder="Search something"
            />
          </div>
        </div>
        <div class="w-30p flex justify-end items-center">
          <div>
            <img class="w-6" src="../assets/images/berle.png" />
          </div>
          <div>
            <img class="w-14 mx-4" src="../assets/images/profile.png" />
          </div>
          <div>
            <div class="black-80 font-bold">Francois AISSAN</div>
            <div class="black-49 font-bold">Data security</div>
          </div>
        </div>
      </div>
      <div class="bket-home-content relative pt-3">
        <router-view></router-view>
        <div
          class="flex justify-center w-full black-20 font-bold absolute -bottom-5 text-xs"
        >
          @ Powered by Bio Market
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import SideBarComponent from "@/components/SideBarComponent.vue";

@Options({
  components: { SideBarComponent },
})
export default class HomeView extends Vue {}
</script>
