<template>
  <div class=" col-9">
    <BannerSidebar />
     <!-- here first section 4 categories-->
    <section-category>
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
     <!-- here second section chioce for you -->
    <section-category>
      <span slot="category-name">
        اخترنا لك
      </span>
      <div class="col-3 category" slot="item">
       <card-item></card-item>
      </div>
      <div class="col-3 category" slot="item">
       <card-item></card-item>
      </div>
      <div class="col-3 category" slot="item">
       <card-item></card-item>
      </div>
      <div class="col-3 category" slot="item">
       <card-item></card-item>
      </div>
    </section-category>
       <section-category>
      <span slot="category-name">
الاكثر مبيعاً
      </span>
        <div class="col-3 category" slot="item">
       <card-item></card-item>
      </div>  <div class="col-3 category" slot="item">
       <card-item></card-item>
      </div>  <div class="col-3 category" slot="item">
       <card-item></card-item>
      </div>  <div class="col-3 category" slot="item">
       <card-item></card-item>
      </div>  <div class="col-3 category" slot="item">
       <card-item></card-item>
      </div>  <div class="col-3 category" slot="item">
       <card-item></card-item>
      </div>  <div class="col-3 category" slot="item">
       <card-item></card-item>
      </div>  <div class="col-3 category" slot="item">
       <card-item></card-item>
      </div>
       </section-category>
  </div>
</template>

<script>
// imports Components |||||||||||||||||||||||||||||||||||||||||||||||||||\\\
import BannerSidebar from "@/components/BannerSidebar.vue";
import SectionCategory from "@/components/Section.vue";
import CardItem from "@/components/cardItem.vue";
// imports images |||||||||||||||||||||||||||||||||||||||||||||||||||
import phones from "@/assets/images/phones.png";
import pcs from "@/assets/images/pcs.png";
import laptops from "@/assets/images/laptops.png";
import mobails from "@/assets/images/mobails.png";
export default {
  components: {
    BannerSidebar,
    SectionCategory,
    CardItem
  },
  data: () => ({
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
  }),
};
</script>

<style>
.category{
  margin-bottom:15px ;
}
</style>
