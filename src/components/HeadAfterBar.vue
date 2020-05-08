<template>
  <div class="headAfterBar">
    <div class="container margin-top-4">
      <div class="row justify-content-start pr-0">
        <div class="col-3 text-right pr-0">
          <img
            class="img-logo "
            src="@/assets/logo.webp"
            alt="logo moov biycle"
          />
        </div>
        <div class="col-7">
          <div class="input-group ">
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
                <font-awesome-icon icon="search" />
              </button>
            </div>
          </div>
        </div>
        <div class="col-2 justify-content-around d-flex align-items-center">
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
export default {};
</script>

<style lang="scss"></style>
