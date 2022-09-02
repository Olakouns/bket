<template>
  <div class="card-dash mr-10">
    <div class="card-dash-left">
      <img src="../assets/images/business.png" />
    </div>
    <div class="card-dash-right">
      <div class="card-dash-right-amount">
        <div class="card-dash-right-amount-1 mr-3">
          <span>3.000.000</span>
        </div>
        <div class="card-dash-right-amount-2">FCFA</div>
      </div>
      <div class="card-dash-name">CHIFFRE D’AFFAIRE</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "DashboardItemComponent",
};
</script>

<style scoped lang="scss">
.card-dash {
  background: #ffffff;
  border-radius: 12px;
  width: 24rem;
  display: flex;
  height: 7rem;

  &-name {
    color: rgba(0, 0, 0, 0.7);
    font-size: 12px;
    font-weight: 700;
    display: flex;
    justify-content: left;
  }

  &-left {
    background: #00a936;
    border-radius: 12px;
    width: 25%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  &-right {
    width: 75%;
    display: flex;
    flex-direction: column;
    //justify-content: center;
    padding: 17px;
    justify-content: space-around;
    &-amount {
      font-weight: 700;
      line-height: 28px;
      letter-spacing: 0.05em;
      color: #00a936;
      display: flex;
      width: 100%;
      justify-content: left;

      &-1 {
        font-size: 30px;
      }
      &-2 {
        font-size: 18px;
        margin-top: -6px;
      }
    }
  }
}
</style>
