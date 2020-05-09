<template>
  <div class="sideBar col-3 pr-0" dir="rtl">
    <ul class="list-group shadow pr-0 text-right">
      <!-- here  is head menu for  list category -->
      <li class="list-group-item rounded-0 head-menu text-light">
        <font-awesome-icon icon="bars" class="text-left" />
        جميع الفئات
      </li>
      <!-- here for loop for show all categories -->
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
    <!-- render sale components  -->
    <sale :discount="discount">
      <!-- 
        here put you want img or anything 
        with name  slot  image-item-sale
      -->
      <img
        slot="image-item-sale"
        :src="imgSideBanner"
        class="w-100"
        alt="side sale bottom side bar"
      />
    </sale>

    <!-- section deals for side bar  -->
    <section-category>
      <span slot="category-name">
        صفقات اليوم
      </span>
      <div class="category col" slot="item">
        <card-item
          :price="250.0"
          :newItem="false"
          :imgSrc="imgSideBanner"
          :itemName="'اسم المنتج يعرض هنا'"
          :oldItem="true"
          :flexCardVertical="false"
        ></card-item>
      </div>
    </section-category>

    <!-- section new products for side bar  -->

    <section-category>
      <span slot="category-name">
        احدث المنتجات
      </span>
      <div
        class="col-12 category category-sideBar"
        slot="item"
        v-for="item in newProducts"
        :key="item.index"
      >
        <card-item
          :price="item.price"
          :newItem="false"
          :imgSrc="imgSideBanner"
          :itemName="item.name"
          :oldItem="false"
          :flexCardVertical="true"
        ></card-item>
      </div>
    </section-category>
  </div>
</template>

<script>
// for import  components
import Sale from "@/components/Sale.vue";
import SectionCategory from "@/components/Section.vue";
import CardItem from "@/components/cardItem.vue";

export default {
  components: {
    Sale,
    SectionCategory,
    CardItem
  },
  data: () => ({
    discount: 50,
    imgSideBanner: "http://icons.iconseeker.com/png/fullsize/cat/watch-cat.png",
    //for section categories in top  side bar
    categories: [
      {
        name: "الذهب والفضة",
        icon: "hand-holding-heart"
      },
      {
        name: "ادوات واجهزة طبية",
        icon: "heartbeat"
      },
      {
        name: "الصيدليات والادوية",
        icon: "allergies"
      },
      {
        name: "الساعات",
        icon: "clock"
      },
      {
        name: "النظارات والعدسات",
        icon: "microscope"
      },
      {
        name: "الذهب والفضة",
        icon: "hand-holding-heart"
      },
      {
        name: "ادوات واجهزة طبية",
        icon: "heartbeat"
      }
    ],
    //for section new product
    newProducts: [
      {
        name: "اسم المنتج يعرض هنا",
        price: "250.00",
        newitem: true,
        flexCardVertical: true
      },
      {
        name: "اسم المنتج يعرض هنا",
        price: "25.00",
        newitem: true,
        flexCardVertical: true
      },
      {
        name: "اسم المنتج يعرض هنا",
        price: "150.00",
        newitem: true,
        flexCardVertical: true
      },
      {
        name: "اسم المنتج يعرض هنا",
        price: "60.00",
        newitem: true,
        flexCardVertical: true
      }
    ]
  })
};
</script>

<style lang="scss"></style>
