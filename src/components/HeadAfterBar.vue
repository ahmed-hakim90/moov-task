<template>
  <div class="headAfterBar">
    <div class="container margin-top-4">
      <div class="row justify-content-start">
        <div class="col-2 text-right">
          <img
            class="img-logo "
            src="@/assets/logo.webp"
            alt="logo moov biycle"
          />
        </div>
        <div class="col-8">
          <div class="input-group mr-4 ">
            <div class="input-group-prepend">
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
                <i class="fa fa-search" dir="rtl" aria-hidden="true"></i>
              </button>
            </div>
          </div>
        </div>
        <div class="col-2 justify-content-around d-flex align-items-center">
          <i class="fa fa-facebook color-secondery " aria-hidden="true"></i>
          <i class="fa fa-twitter color-secondery" aria-hidden="true"></i>
          <i class="fa fa-instagram color-secondery" aria-hidden="true"></i>
          <i
            class="fa fa-snapchat color-secondery text-warning"
            aria-hidden="true"
          ></i>
          <i class="fa fa-bars color-secondery " aria-hidden="true"></i>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
$base-color-icons: #b8b8b8;
.headAfterBar {
  .text-warning {
    color: #e1da22;
  }
  .color-secondery {
    color: $base-color-icons;
  }
  .margin-top-4 {
    margin-top: 40px;
  }
  .img-logo {
    width: 150px;
  }
  .search-btn {
    height: 50px;
    width: 60px;
    background-color: #66286a !important;
    color: #fff !important;
  }
  .search-input {
    height: 50px !important;
  }
  .fa-search {
    transform: rotate(90deg);
  }
  .all-things {
    border-color: #ced4da !important;
  }
}
</style>
