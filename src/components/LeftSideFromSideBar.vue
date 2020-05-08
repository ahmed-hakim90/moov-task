<template>
  <div class=" col-9">
    <div class="banner">
      <div class="container">
        <div class="row">
          <!-- 
          this is highly featrues for us  
          for loop on array cards 
          to show it
         -->
          <div class="col-4" v-for="card in cardsFeatures" :key="card.index">
            <!-- tis is built card featrue  for everyone -->
            <div
              class="card-before-banner text-light  d-flex align-items-center justify-content-center "
            >
              <!-- here icon for card -->
              <font-awesome-icon :icon="['fab', card.icon]" class="ml-4" />
              <!-- here is text for featrue -->
              <span>
                {{ card.title }}
              </span>
            </div>
          </div>
        </div>
      </div>
      <!-- this is image Banner after featrues -->
      <img :src="imgBanner" class="w-100" />
    </div>
    <!-- here first section 4 categories-->
    <section-category>
      <!-- the bottom div is for loop  on  categorySection in data in the bottom -->
      <div
        class="col-3 category"
        slot="item"
        v-for="category in categorySection"
        :key="category.index"
      >
        <img class="w-100" :src="category.imgCat" alt="phones" />
        <div class="card-body mt-2 p-0">
          <button
            type="button"
            class="btn btn-primary border-0 btn-block rounded-0"
          >
            {{ category.nameCat }}
          </button>
        </div>
      </div>
    </section-category>
    <!-- here second section chioce for you 4 items-->
    <section-category>
      <span slot="category-name">
        اخترنا لك
      </span>

      <!--
      here is col-3 if change here change for all section chioce for you 
      the bottom div is for loop  on  itemsChoiceForU in data in the bottom  
      -->
      <div
        class="col-3 category"
        slot="item"
        v-for="item in itemsChoiceForU"
        :key="item.index"
      >
        <!-- here component card item   isRequird price   name  new||old -->
        <card-item
          :price="item.price"
          :newItem="item.newitem"
          :itemName="item.name"
        ></card-item>
      </div>
    </section-category>

    <!-- here section top sell 8 items -->
    <section-category>
      <span slot="category-name">
        الاكثر مبيعاً
      </span>

      <!--
      here is col-3 if change here change for all section top sell  
      the bottom div is for loop  on  itemsTopSell in data in the bottom  
      -->
      <div
        class="col-3 category"
        slot="item"
        v-for="item in itemsTopSell"
        :key="item.index"
      >
        <!-- here component card item   isRequird price   name  new||old -->
        <card-item
          :price="item.price"
          :newItem="item.newitem"
          :itemName="item.name"
        ></card-item>
      </div>
    </section-category>
  </div>
</template>

<script>
// imports Components |||||||||||||||||||||||||||||||||||||||||||||||||||\\\
import SectionCategory from "@/components/Section.vue";
import CardItem from "@/components/cardItem.vue";
// imports images |||||||||||||||||||||||||||||||||||||||||||||||||||
import banner from "@/assets/images/banner.png";
import phones from "@/assets/images/phones.png";
import pcs from "@/assets/images/pcs.png";
import laptops from "@/assets/images/laptops.png";
import mobails from "@/assets/images/mobails.png";
export default {
  components: {
    SectionCategory,
    CardItem,
  },
  data: () => ({
    // for render image to show it in banner
    imgBanner: banner,
    //  belonges for featrues section
    cardsFeatures: [
      {
        title: "  دفع امن 100%",
        icon: "cc-visa",
      },
      {
        title: "  دفع امن 100%",
        icon: "cc-visa",
      },
      {
        title: "  دفع امن 100%",
        icon: "cc-visa",
      },
    ],
    //  4 categories  have it image and button
    categorySection: [
      {
        imgCat: phones,
        nameCat: "الجوالات",
      },
      {
        imgCat: pcs,
        nameCat: "الكمبيوتر",
      },
      {
        imgCat: laptops,
        nameCat: "لاب توب",
      },
      {
        imgCat: mobails,
        nameCat: "سماعات",
      },
    ],
    // item top sell in our store
    itemsTopSell: [
      { name: "اسم المنتج يعرض هنا", price: "250.00", newitem: true,img:phones },
      { name: "اسم المنتج يعرض هنا", price: "25.00", newitem: false ,img:phones},
      { name: "اسم المنتج يعرض هنا", price: "150.00", newitem: true ,img:phones},
      { name: "اسم المنتج يعرض هنا", price: "60.00", newitem: true ,img:phones},
      { name: "اسم المنتج يعرض هنا", price: "71.85", newitem: true ,img:phones},
      { name: "اسم المنتج يعرض هنا", price: "250.00", newitem: true ,img:phones},
      { name: "اسم المنتج يعرض هنا", price: "1007.00", newitem: true ,img:phones},
      { name: "اسم المنتج يعرض هنا", price: "99.00", newitem: false ,img:phones},
    ],
    // for section chioce for u
    itemsChoiceForU: [
      { name: "اسم المنتج يعرض هنا", price: "250.00", newitem: true ,img:pcs},
      { name: "اسم المنتج يعرض هنا", price: "25.00", newitem: false ,img:pcs},
      { name: "اسم المنتج يعرض هنا", price: "150.00", newitem: true ,img:pcs},
      { name: "اسم المنتج يعرض هنا", price: "60.00", newitem: true ,img:pcs},
    ],
  }),
};
</script>

<style>
.card-before-banner {
  /* margin:-15px ; */
  height: 80px;
  background-color: #a580a7;
  margin-bottom: 20px;
  font-size: 20px;
}
.col-4:last-of-type {
  padding-left: 0;
}
.category {
  margin-bottom: 15px;
}
</style>
