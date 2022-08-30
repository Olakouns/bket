<template>
  <div class="flex w-full">
    <div class="w-4/6 bg-orange-800">ok</div>
    <div class="w-2/6 flex flex-col justify-center items-end">
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
  </div>
</template>

<script>
export default {
  name: "DashboardView",
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
</style>
