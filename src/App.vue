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
       <div class="col-3 category" slot="item">
       <card-item></card-item>
      </div> <div class="col-3 category" slot="item">
       <card-item></card-item>
      </div> <div class="col-3 category" slot="item">
       <card-item></card-item>
      </div> <div class="col-3 category" slot="item">
       <card-item></card-item>
      </div>
        </section-category>
    </div>
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
  },
};
</script>

<style lang="scss">
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  direction: rtl;
}
</style>
