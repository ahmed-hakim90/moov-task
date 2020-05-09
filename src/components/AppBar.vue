<template>
  <div class="border-bottom" :class="headAppFixied ? 'mobail bg-white' : ''">
    <div :class="headAppFixied ? 'container-fluid' : 'container'">
      <nav class="row">
        <div
          class="nav col-12 col-lg-6 pr-0 justify-content-center justify-content-lg-start"
          v-if="!headAppFixied"
        >
          <a class="nav-link" href="#">
            توصيل سريع يصل الي 3 ساعات
          </a>

          <a class="nav-link" href="#">
            شحن مجاني للطلبات بقيمة 50 ريال
          </a>
        </div>

        <div
          class="nav col-12 col-lg-6 justify-content-center justify-content-lg-end"
        >
          <a class="nav-link " href="#">
            تسجيل
          </a>

          <a class="nav-link" href="#">
            تسجيل الدخول
          </a>

          <a class="nav-link active" href="#"> البيع علي منصة موف ستور </a>
          <!-- here intaractive lang switch if you wants -->
          <select class="bg-transparent border-0" v-model="selected">
            <option value="EN">EN</option>
            <option value="AR">AR</option>
            <option value="GR">GR</option>
          </select>
        </div>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    selected: "EN",
    headAppFixied: false,
    width: 0
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
.mobail {
  top: 0;
  z-index: 10;
  width: 100%;
  position: fixed;
  background-color: #fff;
}
</style>
