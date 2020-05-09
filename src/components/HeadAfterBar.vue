<template>
  <div
    class="headAfterBar "
    :class="headAppFixied ? 'headMob shadow-bottom' : ''"
  >
    <div
      :class="
        headAppFixied ? 'mt-0  container-fluid' : 'container margin-top-4'
      "
    >
      <div
        class=""
        :class="headAppFixied ? 'row ' : 'row justify-content-start pr-0'"
      >
        <div class="col-3 text-right pr-0" v-if="!headAppFixied">
          <!-- 
            this is img logo in after nav  in right top
           -->
          <img
            class="img-logo "
            src="@/assets/logo.webp"
            alt="logo moov biycle"
          />
        </div>
        <!-- 
          here input and 2 button  1 for categories and 1 for submit search
         -->
        <div :class="headAppFixied ? 'col-12 p-0' : 'col-7'">
          <div class="input-group ">
            <div class="input-group-prepend">
              <!-- here button dropdown list for select item -->
              <button
                class="btn btn-outline-secondary all-things border-left-0 rounded-0 dropdown-toggle"
                type="button"
                data-toggle="dropdown"
                aria-haspopup="true"
                aria-expanded="false"
              >
                جميع الفئات
              </button>
              <div class="dropdown-menu">
                <a class="dropdown-item" href="#">Action</a>
              </div>
            </div>
            <input
              type="text"
              class="form-control border-right-0 search-input rounded-0"
              aria-label="Text input with dropdown button"
              placeholder="ابحث في الاقسام الخاصة بنا"
            />
            <div class="input-group-append">
              <button class="btn search-btn rounded-0" type="button">
                <font-awesome-icon icon="search" />
              </button>
            </div>
          </div>
        </div>
        <div
          class="col-2 justify-content-around d-flex align-items-center"
          v-if="!headAppFixied"
        >
          <font-awesome-icon :icon="['fab', 'instagram']" />
          <font-awesome-icon :icon="['fab', 'facebook-f']" />
          <font-awesome-icon :icon="['fab', 'twitter']" />
          <font-awesome-icon :icon="['fab', 'snapchat']" class="text-warning" />
          <font-awesome-icon :icon="['fas', 'bars']" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
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
      } else {
        this.headAppFixied = false;
      }
    }
  }
};
</script>

<style lang="scss">
.headMob {
  top: 57px;
  left: 0;
  width: 100%;
  position: fixed;
  z-index: 11;
  background-color: #fff;
  box-shadow: 0 2px 0.5rem #ddd;
}
</style>
