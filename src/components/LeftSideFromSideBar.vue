<template>
  <div
    class=" col-12 col-md-9 "
    :class="headAppFixied ? 'margin-in-mobail' : ''"
  >
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
        class="col-6 col-md-4 col-lg-3 category"
        slot="item"
        v-for="category in categorySection"
        :key="category.index"
      >
        <img class="w-100" :src="imgWatch" alt="phones" />
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
        class="col-6 col-md-4 col-lg-3 category"
        slot="item"
        v-for="item in itemsChoiceForU"
        :key="item.index"
      >
        <!-- here component card item   isRequird price   name  new||old -->
        <card-item
          :price="item.price"
          :newItem="item.newitem"
          :itemName="item.name"
          :imgSrc="imgWatch"
        ></card-item>
      </div>
    </section-category>
    <!--Small banner 2 banner -->
    <div class="row">
      <div class="banner banner-middle col-12 mt-4 mt-sm-0 col-sm-6 ">
        <div class="bg-secondary text-right p-2">
          <div class="content-banner">
            <!-- img background -->
            <p class="p-2 p-sm-4 h4 text-light ">
              تابع احدث كولكشن سماعات
            </p>
            <button
              type="button"
              class="btn btn-main text-light pl-4 pr-4  border-0 rounded-0"
            >
              اقرا المزيد
            </button>
          </div>
        </div>
      </div>
      <div class="banner banner-middle col-12  pt-2 pt-sm-0 col-sm-6 ">
        <div class="bg-secondary text-right p-2 ">
          <div class="content-banner">
            <!-- img background -->
            <p class="p-2 p-sm-4 h4 text-light ">
              تابع احدث كولكشن سماعات
            </p>
            <button
              type="button"
              class="btn btn-main text-light pl-4 pr-4  border-0 rounded-0"
            >
              اقرا المزيد
            </button>
          </div>
        </div>
      </div>
    </div>
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
        class="col-6 col-md-4 col-lg-3 category"
        slot="item"
        v-for="item in itemsTopSell"
        :key="item.index"
      >
        <!-- here component card item   isRequird price   name  new||old -->
        <card-item
          :price="item.price"
          :newItem="item.newitem"
          :itemName="item.name"
          :imgSrc="imgWatch"
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

export default {
  components: {
    SectionCategory,
    CardItem
  },
  data: () => ({
    headAppFixied: false,
    width: 0,
    // for render image to show it in banner
    imgBanner: banner,
    imgWatch: `https://moovstore-images.s3.amazonaws.com/attachments/images/Apr/Alighanem/20200428194136_1372451588095696.webp?X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIA2AAKYE2C2IA3FWS5%2F20200508%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20200508T225343Z&X-Amz-SignedHeaders=host&X-Amz-Expires=518400&X-Amz-Signature=def7a9f70aaea67509b37cd37d33b3e6e112d0dfe3f62fe26f59abf077f36c55
`,
    //  belonges for featrues section
    cardsFeatures: [
      {
        title: "  دفع امن 100%",
        icon: "cc-visa"
      },
      {
        title: "  دفع امن 100%",
        icon: "cc-visa"
      },
      {
        title: "  دفع امن 100%",
        icon: "cc-visa"
      }
    ],
    //  4 categories  have it image and button
    categorySection: [
      {
        imgCat: "",
        nameCat: "الجوالات"
      },
      {
        imgCat: "cs",
        nameCat: "الكمبيوتر"
      },
      {
        imgCat: "laptops",
        nameCat: "لاب توب"
      },
      {
        imgCat: "mobails",
        nameCat: "سماعات"
      }
    ],
    // item top sell in our store
    itemsTopSell: [
      {
        name: "اسم المنتج يعرض هنا",
        price: "250.00",
        newitem: true
      },
      {
        name: "اسم المنتج يعرض هنا",
        price: "25.00",
        newitem: false
      },
      {
        name: "اسم المنتج يعرض هنا",
        price: "150.00",
        newitem: true
      },
      {
        name: "اسم المنتج يعرض هنا",
        price: "60.00",
        newitem: true
      },
      {
        name: "اسم المنتج يعرض هنا",
        price: "71.85",
        newitem: true
      },
      {
        name: "اسم المنتج يعرض هنا",
        price: "250.00",
        newitem: true
      },
      {
        name: "اسم المنتج يعرض هنا",
        price: "1007.00",
        newitem: true
      },
      {
        name: "اسم المنتج يعرض هنا",
        price: "99.00",
        newitem: false
      }
    ],
    // for section chioce for u
    itemsChoiceForU: [
      { name: "اسم المنتج يعرض هنا", price: "250.00", newitem: true },
      { name: "اسم المنتج يعرض هنا", price: "25.00", newitem: false },
      { name: "اسم المنتج يعرض هنا", price: "150.00", newitem: true },
      { name: "اسم المنتج يعرض هنا", price: "60.00", newitem: true }
    ]
  }),
  created() {
    window.addEventListener("resize", this.handleResize);
    this.handleResize();
  },
  destroyed() {
    window.removeEventListener("resize", this.handleResize);
  },
  methods: {
    handleResize() {
      this.width = window.innerWidth;
      if (this.width <= 755) {
        this.headAppFixied = true;
        console.log(this.headAppFixied);
      } else {
        this.headAppFixied = false;
      }
    }
  }
};
</script>

<style lang="scss">
.margin-in-mobail {
  margin-top: 90px;
  .card-before-banner {
    height: 60px;
    font-size: 16px;
    svg {
      margin-left: 10px !important;
    }
  }
}
.banner-middle {
  .bg-secondary {
    height: 170px;
  }
  .content-banner {
    margin: auto;
  }
}
.banner.banner-middle.col-12.mt-4.mt-sm-0.col-sm-6 {
  padding-right: 15px !important;
}
</style>
