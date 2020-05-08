<template>
  <div class="sideBar col-3 pr-0" dir="rtl">
    <ul class="list-group pr-0 text-right">
      <li class="list-group-item rounded-0 head-menu text-light">
        <font-awesome-icon icon="bars" class="text-left" />
        جميع الفئات
      </li>
      <li
        class="list-group-item justify-content-between d-flex"
        v-for="cat in categories"
        :key="cat.index"
      >
        <div>
          <font-awesome-icon :icon="cat.icon" />
          {{ cat.name }}
        </div>
        <font-awesome-icon icon="angle-left" class="text-left" />
      </li>
    </ul>
   <Sale  :discount="discount" >
      <img slot="image-item-sale" :src="imgSideBanner" class="w-100" alt="side sale bottom side bar" />
      </Sale>
    </div>
</template>

<script>
// for card discount 
import Sale from "@/components/Sale.vue";
// import image from assers to  show it in com
import sideBanner from "@/assets/images/20200506205139_648991588791099.webp";
export default {
  components: {
   Sale
  },
  data: () => ({
    discount:50,
    imgSideBanner: sideBanner,
    categories: [
      {
        name: "الذهب والفضة",
        icon: "hand-holding-heart",
      },
      {
        name: "ادوات واجهزة طبية",
        icon: "",
      },
      {
        name: "الصيدليات والادوية",
        icon: "",
      },
      {
        name: "الساعات",
        icon: "",
      },
      {
        name: "النظارات والعدسات",
        icon: "",
      },
      {
        name: "الذهب والفضة",
        icon: "hand-holding-heart",
      },
      {
        name: "ادوات واجهزة طبية",
        icon: "",
      },
    ],
  }),
};
</script>

<style lang="scss"></style>
