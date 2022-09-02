<template>
  <div class="flex justify-between product-item items-center p-3 mb-3">
    <div class="flex items-center w-3/4 justify-between">
      <div class="w-1/6">
        <img
          class=""
          :style="{ width: product.size }"
          :src="require('../assets/images/' + product.image)"
        />
      </div>

      <div class="w-1/6">
        <div
          class="product-item-line"
          :style="{ background: product.colorStyle }"
        ></div>
      </div>

      <div class="product-item-text product-item-text-1 w-2/6">
        {{ product.name }}
      </div>
      <div class="product-item-text" :style="{ color: product.colorStyle }">
        {{ product.category }}
      </div>
    </div>
    <div class="w-1/4 flex justify-end">
      <button class="mr-4">
        <svg
          width="27"
          height="27"
          viewBox="0 0 17 17"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <circle cx="8.5" cy="8.5" r="8.5" fill="#D9D9D9" />
          <path
            d="M11.9886 5H11.1543L6.44001 9.71429L6.34856 9.83998L5 12.1943L5.80573 13L8.16002 11.6514L8.28571 11.56L13 6.8457V6.01144L11.9886 5ZM5.80573 12.1943L6.6686 10.48L7.49714 11.3086L5.80573 12.1943ZM7.99428 11.0172L6.98284 10.0057L11.5543 5.43429L12.5657 6.44573L7.99428 11.0172Z"
            fill="black"
            fill-opacity="0.8"
          />
        </svg>
      </button>
      <button>
        <svg
          width="23"
          height="25"
          viewBox="0 0 11 13"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            fill-rule="evenodd"
            clip-rule="evenodd"
            d="M8 2H10H11V3H10V12L9 13H2L1 12V3H0V2H3V1C3 0.734784 3.10531 0.480383 3.29285 0.292847C3.48038 0.10531 3.73478 0 4 0H7C7.26522 0 7.51962 0.10531 7.70715 0.292847C7.89469 0.480383 8 0.734784 8 1V2ZM7 1H4V2H7V1ZM2 12H9V3H2V12ZM4 4H3V11H4V4ZM5 4H6V11H5V4ZM7 4H8V11H7V4Z"
            fill="#E1390D"
          />
        </svg>
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProductComponent",
  props: ["product"],
};
</script>

<style scoped lang="scss">
.product-item {
  background: rgba(255, 255, 255, 0.8);
  border-radius: 6px;
  &-image {
    width: 4rem;
  }
  &-line {
    width: 6px;
    height: 30px;
    border-radius: 8px;
  }

  &-text {
    font-weight: 700;
    &-1 {
      color: rgba(0, 0, 0, 0.8);
    }
  }
}
</style>
