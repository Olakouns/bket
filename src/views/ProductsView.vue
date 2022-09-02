<template>
  <div class="flex w-full h-full flex-col">
    <div class="flex justify-between w-full items-center h-10">
      <div class="flex">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke-width="1.5"
          stroke="currentColor"
          class="w-6 h-6"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M6.75 15.75L3 12m0 0l3.75-3.75M3 12h18"
          />
        </svg>
        <span class="ml-2 black-80 font-bold">Liste des produits</span>
      </div>
      <div>
        <button class="flex btn-add-product text-white p-2">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="w-6 h-6 font-bold"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M12 4.5v15m7.5-7.5h-15"
            />
          </svg>
          <span class="ml-2 font-bold">Ajouter une categorie</span>
        </button>
      </div>
    </div>

    <div class="flex flex-wrap mt-3 h-full">
      <div class="w-3/5">
        <div>
          <button class="flex btn-add-product text-white p-2 pl-4 pr-4">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              class="w-6 h-6 font-bold"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="M12 4.5v15m7.5-7.5h-15"
              />
            </svg>
            <span class="ml-2 font-bold">Ajouter</span>
          </button>
        </div>

        <div class="mt-3">
          <template v-for="(product, index) in products" :key="index">
            <ProductComponent :product="product" />
          </template>
        </div>
      </div>
      <div class="w-2/5 flex flex-col items-end">
        <div
          class="h-2/3 w-4/5 p-3 cat-card mb-3 flex flex-wrap justify-evenly items-center"
        >
          <template v-for="category in categories" :key="category">
            <div class="category-card h-fit w-2/5 flex flex-col justify-center">
              <div
                class="category-card-header p-3 flex justify-center"
                :style="{ background: category.bgColor }"
              >
                <img
                  class=""
                  :style="{ width: category.size }"
                  :src="require('../assets/images/' + category.image)"
                />
              </div>
              <div class="p-3 text-center font-bold">{{ category.name }}</div>
            </div>
          </template>
        </div>
        <div
          class="h-1/3 bottom-card flex flex-col justify-center items-center w-4/5 p-3"
        >
          <div>
            <img class="w-40" src="../assets/images/tomato.png" />
          </div>
          <div class="text-white text-center">
            La tomate est excellente pour attaquer les mauvaises graisses et les
            éliminer plus facilement.
          </div>
          <div class="flex mt-3 mb-3">
            <div class="roundedSmall roundedSmall-1 mr-3"></div>
            <div class="roundedSmall roundedSmall-2 mr-3"></div>
            <div class="roundedSmall roundedSmall-2"></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ProductComponent from "@/components/ProductComponent";

export default {
  name: "ProductsView",
  components: { ProductComponent },
  data() {
    return {
      products: [
        {
          image: "tomato.png",
          name: "Tomates",
          category: "Fruits",
          colorStyle: "#E1390D",
          size: "6rem",
        },
        {
          image: "bananas.png",
          name: "Banane",
          category: "Fruits",
          colorStyle: "#D6B441",
          size: "5rem",
        },
        {
          image: "avocado.png",
          name: "Avocats",
          category: "Fruits",
          colorStyle: "#3F4D2C",
          size: "4.5rem",
        },
        {
          image: "orange.png",
          name: "Orange",
          category: "Fruits",
          colorStyle: "#D37715",
          size: "4rem",
        },
        {
          image: "papaya.png",
          name: "Papaye",
          category: "Fruits",
          colorStyle: "#3A1D11",
          size: "6rem",
        },
        {
          image: "avocado.png",
          name: "Avocats",
          category: "Fruits",
          colorStyle: "#3F4D2C",
          size: "4.5rem",
        },
      ],
      categories: [
        {
          image: "all-fruits.png",
          name: "LES FRUITS",
          bgColor: "rgba(240, 141, 90, 0.51)",
          size: "6rem",
        },
        {
          image: "basilic.png",
          name: "LES LEGUMES",
          bgColor: "rgba(167, 183, 141, 0.51)",
          size: "4rem",
        },
        {
          image: "basilic.png",
          name: "LES LEGUMES",
          bgColor: "rgba(167, 183, 141, 0.51)",
          size: "4rem",
        },
        {
          image: "all-fruits.png",
          name: "LES FRUITS",
          bgColor: "rgba(240, 141, 90, 0.51)",
          size: "6rem",
        },
        {
          image: "all-fruits.png",
          name: "LES FRUITS",
          bgColor: "rgba(240, 141, 90, 0.51)",
          size: "6rem",
        },
        {
          image: "basilic.png",
          name: "LES LEGUMES",
          bgColor: "rgba(167, 183, 141, 0.51)",
          size: "4rem",
        },
        // {
        //   image: "all-fruits.png",
        //   name: "LES FRUITS",
        //   bgColor: "rgba(240, 141, 90, 0.51)",
        //   size: "6rem",
        // },
        // {
        //   image: "all-fruits.png",
        //   name: "LES FRUITS",
        //   bgColor: "rgba(240, 141, 90, 0.51)",
        //   size: "6rem",
        // },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
.btn-add-product {
  background: #00a936;
  border-radius: 8px;
}

.bottom-card {
  background: rgba(0, 169, 54, 0.6);
  border-radius: 8px;
}
.roundedSmall {
  width: 0.7rem;
  height: 0.7rem;
  border-radius: 50%;
  &-1 {
    background-color: #ffffff;
  }
  &-2 {
    background-color: #d9d9d9;
  }
}

.cat-card {
  background: #ffffff;
  border-radius: 8px;
}

.category-card {
  background: rgba(217, 217, 217, 0.8);
  border-radius: 12px;
  &-header {
    //background: rgba(240, 141, 90, 0.51);
    border-radius: 12px 12px 0px 0px;
  }
}
</style>
