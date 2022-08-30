<template>
  <div class="relative w-full">
    <div class="bket-side-bar-header flex items-center mb-8">
      <img src="../assets/images/bket_left.png" class="w-8 mr-3" />
      <img src="../assets/images/Bket_logo_g.png" class="w-16" />
    </div>
    <div class="bket-side-bar-content">
      <div class="flex flex-col">
        <template v-for="menu in menuList" :key="menu.title">
          <template v-if="!menu.hasSubMenu">
            <router-link
              :to="menu.link"
              class="bket-side-bar-menu flex items-center p-2 w-full mb-2"
              active-class="bket-side-bar-menu-active"
            >
              <div
                class="bket-side-bar-menu-icon mx-3"
                v-html="menu.icon"
              ></div>
              <label class="bket-side-bar-menu-text"> {{ menu.title }} </label>
            </router-link>
          </template>
          <template v-else>
            <AccordionComponent class="mb-2" :title="menu.title">
              <template v-for="sub in menu.subMenu" :key="sub.link">
                <router-link
                  :to="sub.link"
                  class="bket-side-bar-menu-2 flex items-center p-2 w-full"
                  active-class="bket-side-bar-menu-2-active"
                >
                  <div class="bket-side-bar-menu-2 left-pane"></div>
                  <div>{{ sub.title }}</div>
                </router-link>
              </template>
            </AccordionComponent></template
          >
        </template>
      </div>
    </div>

    <div class="absolute bottom-12 right-0 w-full flex justify-center">
      <router-link to="" class="flex items-center pointer">
        <div class="mr-3">
          <svg
            width="24"
            height="24"
            viewBox="0 0 24 24"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M19.85 8.75L24 9.57996V14.42L19.85 15.25L22.2 18.77L18.77 22.2L15.25 19.85L14.42 24H9.57996L8.75 19.85L5.22998 22.2L1.80005 18.77L4.15002 15.25L0 14.42V9.57996L4.15002 8.75L1.80005 5.22998L5.22998 1.80005L8.75 4.15002L9.57996 0H14.42L15.25 4.15002L18.77 1.80005L22.2 5.22998L19.85 8.75ZM18.28 13.8199L22.28 13.01V11.01L18.28 10.2L17.74 8.90002L20.03 5.46997L18.6 4.04004L15.17 6.32996L13.87 5.79004L13.0601 1.79004H11.0601L10.25 5.79004L8.94995 6.32996L5.52002 4.04004L4.08997 5.46997L6.38 8.90002L5.83997 10.2L1.83997 11.01V13.01L5.83997 13.8199L6.38 15.12L4.08997 18.55L5.52002 19.98L8.94995 17.6899L10.25 18.23L11.0601 22.23H13.0601L13.87 18.23L15.17 17.6899L18.6 19.98L20.03 18.55L17.74 15.12L18.28 13.8199ZM10.0943 9.14807C10.6584 8.77118 11.3216 8.56995 12 8.56995C12.9089 8.57258 13.7798 8.93484 14.4225 9.57751C15.0652 10.2202 15.4274 11.0911 15.43 12C15.43 12.6784 15.2288 13.3416 14.8519 13.9056C14.475 14.4697 13.9394 14.9093 13.3126 15.1689C12.6859 15.4286 11.9962 15.4965 11.3308 15.3641C10.6654 15.2318 10.0543 14.9051 9.57457 14.4254C9.09488 13.9457 8.7682 13.3345 8.63585 12.6692C8.50351 12.0038 8.57143 11.3141 8.83104 10.6874C9.09065 10.0606 9.53029 9.52496 10.0943 9.14807ZM11.0499 13.4218C11.3311 13.6097 11.6618 13.71 12 13.71C12.2249 13.7113 12.4479 13.668 12.656 13.5825C12.8641 13.4971 13.0531 13.3712 13.2121 13.2122C13.3712 13.0531 13.497 12.8641 13.5825 12.656C13.668 12.4479 13.7113 12.2249 13.7099 12C13.7099 11.6618 13.6096 11.3311 13.4217 11.0499C13.2338 10.7687 12.9669 10.5496 12.6544 10.4202C12.3419 10.2907 11.9981 10.2569 11.6664 10.3229C11.3347 10.3889 11.03 10.5517 10.7909 10.7909C10.5517 11.03 10.3888 11.3347 10.3229 11.6664C10.2569 11.9981 10.2907 12.342 10.4202 12.6544C10.5496 12.9669 10.7687 13.2339 11.0499 13.4218Z"
              fill="black"
              fill-opacity="0.8"
            />
          </svg>
        </div>

        <label>Parametre</label>
      </router-link>
    </div>
  </div>
</template>

<script>
import AccordionComponent from "@/components/AccordionComponent";

export default {
  name: "SideBarComponent",
  components: { AccordionComponent },
  data() {
    return {
      menuList: [
        {
          icon:
            "<svg\n" +
            '              width="17"\n' +
            '              height="16"\n' +
            '              viewBox="0 0 17 16"\n' +
            '              fill="white"\n' +
            '              xmlns="http://www.w3.org/2000/svg"\n' +
            "            >\n" +
            "              <path\n" +
            '                fill-rule="evenodd"\n' +
            '                clip-rule="evenodd"\n' +
            '                d="M9.5625 1L10.625 0H15.9375L17 1V6L15.9375 7H10.625L9.5625 6V1ZM10.625 1V6H15.9375V1H10.625ZM0 10V4L1.0625 3H6.375L7.4375 4V9H12.75L13.8125 10V15L12.75 16H7.4375H6.375H1.0625L0 15V10ZM6.375 9V4H1.0625V9H6.375ZM6.375 10H1.0625V15H6.375V10ZM7.4375 15H12.75V10H7.4375V15Z"\n' +
            "              />\n" +
            "            </svg>",
          title: "Tableau de bord",
          link: "/home",
          hasSubMenu: false,
        },
        {
          icon:
            '<svg width="16" height="18" viewBox="0 0 16 18" fill="black" xmlns="http://www.w3.org/2000/svg">\n' +
            '<path d="M15.3456 3.93874L8.66778 0H7.33222L0.654412 3.93874L0 5.06783V12.9453L0.654412 14.0613L7.33222 18H8.66778L15.3456 14.0613L16 12.9453V5.06783L15.3456 3.93874ZM7.33222 16.4903L1.32219 12.9453V6.17063L7.33222 9.38737V16.4903ZM1.66945 4.85772L8 1.12909L14.3305 4.85772L8 8.25828L1.66945 4.85772ZM14.6778 12.9453L8.66778 16.4903V9.38737L14.6778 6.17063V12.9453Z"/>\n' +
            "</svg>\n",
          title: "Gestion des produits",
          link: "/products",
          hasSubMenu: false,
        },
        {
          icon:
            '<svg width="20" height="14" viewBox="0 0 20 14" fill="black" xmlns="http://www.w3.org/2000/svg">\n' +
            '<path fill-rule="evenodd" clip-rule="evenodd" d="M7 7C8.93 7 10.5 5.43 10.5 3.5C10.5 1.57 8.93 0 7 0C5.07 0 3.5 1.57 3.5 3.5C3.5 5.43 5.07 7 7 7ZM0 12.25C0 9.92 4.66 8.75 7 8.75C9.34 8.75 14 9.92 14 12.25V14H0V12.25ZM7 10.75C5.21 10.75 3.18 11.42 2.34 12H11.66C10.82 11.42 8.79 10.75 7 10.75ZM8.5 3.5C8.5 2.67 7.83 2 7 2C6.17 2 5.5 2.67 5.5 3.5C5.5 4.33 6.17 5 7 5C7.83 5 8.5 4.33 8.5 3.5ZM14.04 8.81C15.2 9.65 16 10.77 16 12.25V14H20V12.25C20 10.23 16.5 9.08 14.04 8.81ZM16.5 3.5C16.5 5.43 14.93 7 13 7C12.46 7 11.96 6.87 11.5 6.65C12.13 5.76 12.5 4.67 12.5 3.5C12.5 2.33 12.13 1.24 11.5 0.35C11.96 0.13 12.46 0 13 0C14.93 0 16.5 1.57 16.5 3.5Z"/>\n' +
            "</svg>\n",
          title: "Gestion des clients",
          link: "/clients",
          hasSubMenu: false,
        },
        {
          icon:
            '<svg width="20" height="14" viewBox="0 0 20 14" fill="black" xmlns="http://www.w3.org/2000/svg">\n' +
            '<path fill-rule="evenodd" clip-rule="evenodd" d="M7 7C8.93 7 10.5 5.43 10.5 3.5C10.5 1.57 8.93 0 7 0C5.07 0 3.5 1.57 3.5 3.5C3.5 5.43 5.07 7 7 7ZM0 12.25C0 9.92 4.66 8.75 7 8.75C9.34 8.75 14 9.92 14 12.25V14H0V12.25ZM7 10.75C5.21 10.75 3.18 11.42 2.34 12H11.66C10.82 11.42 8.79 10.75 7 10.75ZM8.5 3.5C8.5 2.67 7.83 2 7 2C6.17 2 5.5 2.67 5.5 3.5C5.5 4.33 6.17 5 7 5C7.83 5 8.5 4.33 8.5 3.5ZM14.04 8.81C15.2 9.65 16 10.77 16 12.25V14H20V12.25C20 10.23 16.5 9.08 14.04 8.81ZM16.5 3.5C16.5 5.43 14.93 7 13 7C12.46 7 11.96 6.87 11.5 6.65C12.13 5.76 12.5 4.67 12.5 3.5C12.5 2.33 12.13 1.24 11.5 0.35C11.96 0.13 12.46 0 13 0C14.93 0 16.5 1.57 16.5 3.5Z"/>\n' +
            "</svg>\n",
          title: "Gestion des utilisateurs",
          link: "/users",
          hasSubMenu: false,
        },
        {
          icon:
            '<svg width="16" height="18" viewBox="0 0 16 18" fill="black" xmlns="http://www.w3.org/2000/svg">\n' +
            '<path d="M15.3456 3.93874L8.66778 0H7.33222L0.654412 3.93874L0 5.06783V12.9453L0.654412 14.0613L7.33222 18H8.66778L15.3456 14.0613L16 12.9453V5.06783L15.3456 3.93874ZM7.33222 16.4903L1.32219 12.9453V6.17063L7.33222 9.38737V16.4903ZM1.66945 4.85772L8 1.12909L14.3305 4.85772L8 8.25828L1.66945 4.85772ZM14.6778 12.9453L8.66778 16.4903V9.38737L14.6778 6.17063V12.9453Z""/>\n' +
            "</svg>\n",
          title: "Gestion des ventes",
          link: "",
          hasSubMenu: true,
          subMenu: [
            {
              title: "Vendre un produit",
              link: "/sale-products",
            },
            {
              title: "Lister les ventes",
              link: "/sales",
            },
          ],
        },
        {
          icon:
            '<svg width="20" height="14" viewBox="0 0 20 14" fill="black" xmlns="http://www.w3.org/2000/svg">\n' +
            '<path fill-rule="evenodd" clip-rule="evenodd" d="M7 7C8.93 7 10.5 5.43 10.5 3.5C10.5 1.57 8.93 0 7 0C5.07 0 3.5 1.57 3.5 3.5C3.5 5.43 5.07 7 7 7ZM0 12.25C0 9.92 4.66 8.75 7 8.75C9.34 8.75 14 9.92 14 12.25V14H0V12.25ZM7 10.75C5.21 10.75 3.18 11.42 2.34 12H11.66C10.82 11.42 8.79 10.75 7 10.75ZM8.5 3.5C8.5 2.67 7.83 2 7 2C6.17 2 5.5 2.67 5.5 3.5C5.5 4.33 6.17 5 7 5C7.83 5 8.5 4.33 8.5 3.5ZM14.04 8.81C15.2 9.65 16 10.77 16 12.25V14H20V12.25C20 10.23 16.5 9.08 14.04 8.81ZM16.5 3.5C16.5 5.43 14.93 7 13 7C12.46 7 11.96 6.87 11.5 6.65C12.13 5.76 12.5 4.67 12.5 3.5C12.5 2.33 12.13 1.24 11.5 0.35C11.96 0.13 12.46 0 13 0C14.93 0 16.5 1.57 16.5 3.5Z"  fill-opacity="0.65"/>\n' +
            "</svg>\n",
          title: "Gestion des fournisseurs",
          link: "/providers",
          hasSubMenu: false,
        },
      ],
    };
  },
};
</script>

<style scoped></style>
