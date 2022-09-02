<template>
  <div class="flex w-full h-full">
    <div class="w-4/6">
      <div class="flex w-full">
        <DashboardItemComponent />
        <DashboardItemComponent />
      </div>
    </div>
    <div class="w-2/6 flex flex-col justify-center items-end">
      <div class="h-80">
        <div class="flex w-100 justify-center">
          <img class="w-96" src="../assets/images/tomato.png" />
        </div>
        <div class="custom-card w-96 p-3">
          <div class="flex items-center justify-center">
            <span class="mr-3 label"
              ><label class="label-1">Plus de 1 200 000 </label
              ><label class="label-2">ventes de sac</label></span
            >
            <img src="../assets/images/cover_mounth.png" />
          </div>
        </div>
      </div>

      <div
        class="mt-3 glob w-96 relative flex flex-col items-center justify-evenly"
      >
        <img class="w-1/2" src="../assets/images/glob.png" alt="globe" />
        <div class="w-3/4 text-center">
          <span class="text-white"
            >Retrouvez <span class="font-bold">Bkiet</span> partout dans le
            monde en un seul click</span
          >
        </div>
        <div class="w-5 h-5 bg-white circle absolute"></div>
      </div>
    </div>
  </div>
</template>

<script>
import DashboardItemComponent from "@/components/DashboardItemComponent";

export default {
  name: "DashboardView",
  components: { DashboardItemComponent },
};
</script>

<style scoped lang="scss">
.custom-card {
  background: #ffffff;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.08);
  border-radius: 8px;
}

.label {
  font-weight: 700;
  font-size: 13px;
  line-height: 12px;
  &-1 {
    color: #e1390d;
  }
  &-2 {
    color: rgba(0, 0, 0, 0.7);
  }
}

.glob {
  background: rgba(0, 169, 54, 0.6);
  border-radius: 8px;
  height: calc(100% - 20rem);
}
.circle {
  border-radius: 50%;
  top: 16px;
  right: 16px;
}
</style>
