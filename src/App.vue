<template>
  <div id="app">
    <app-bar />
    <HeadAfterBar />
    <div class="container margin-top-4">
      <div class="row">
        <side-bar />
        <left-side></left-side>
        <div class="col-3">
          <Sale :discount="50">
            <img
              slot="image-item-sale"
              class="card-img-top bg-transparent h-80"
              src="@/assets/images/20200506205139_648991588791099.webp"
              alt=""
            />
          </Sale>
        </div>
        <div class="col-3">
          <Sale :discount="35">
            <img
              slot="image-item-sale"
              class="card-img-top bg-transparent h-80"
              src="@/assets/images/20200506205139_648991588791099.webp"
              alt=""
            />
          </Sale>
        </div>
        <div class="col-3">
          <Sale :discount="50">
            <img
              slot="image-item-sale"
              class="card-img-top bg-transparent h-80"
              src="@/assets/images/20200506205139_648991588791099.webp"
              alt=""
            />
          </Sale>
        </div>
        <div class="col-3">
          <Sale :discount="60">
            <img
              slot="image-item-sale"
              class="card-img-top bg-transparent h-80"
              src="@/assets/images/20200506205139_648991588791099.webp"
              alt=""
            />
          </Sale>
        </div>
      </div>
      <section-category>
        <span slot="category-name">
          الكترونيات
        </span>
        <div
          class="col category"
          slot="item"
          v-for="item in items"
          :key="item.index"
        >
          <card-item
            :price="item.price"
            :newItem="item.newitem"
            :itemName="item.name"
            :imgSrc="imgWatch"
          >
          </card-item>
        </div>
      </section-category>
    </div>
    <app-footer> </app-footer>
  </div>
</template>

<script>
import AppBar from "./components/AppBar.vue";
import HeadAfterBar from "./components/HeadAfterBar.vue";
import SideBar from "./components/SideBar.vue";
import LeftSide from "./components/LeftSideFromSideBar.vue";
import Sale from "./components/Sale";
import SectionCategory from "@/components/Section.vue";
import CardItem from "@/components/cardItem.vue";
import AppFooter from "@/components/AppFooter.vue";
export default {
  name: "App",
  components: {
    AppBar,
    HeadAfterBar,
    SideBar,
    LeftSide,
    Sale,
    SectionCategory,
    CardItem,
    AppFooter,
  },
  data: () => ({
    imgWatch: `https://moovstore-images.s3.amazonaws.com/attachments/images/Apr/Alighanem/20200428194136_1372451588095696.webp?X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIA2AAKYE2C2IA3FWS5%2F20200508%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20200508T225343Z&X-Amz-SignedHeaders=host&X-Amz-Expires=518400&X-Amz-Signature=def7a9f70aaea67509b37cd37d33b3e6e112d0dfe3f62fe26f59abf077f36c55
`,
    items: [
      { name: "اسم المنتج يعرض هنا", price: "200.00", newitem: true },
      { name: "اسم المنتج يعرض هنا", price: "150.00", newitem: true },
      { name: "اسم المنتج يعرض هنا", price: "50.00", newitem: true },
      { name: "اسم المنتج يعرض هنا", price: "350.00", newitem: true },
      { name: "اسم المنتج يعرض هنا", price: "350.00", newitem: true },
    ],
  }),
};
</script>

<style lang="scss"></style>
