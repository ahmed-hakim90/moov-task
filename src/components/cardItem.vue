<template>
  <div class="card  rounded-0 position-relative">
    <span class="new border-bottom border-top text-center mt-2 ml-2 mr-2">
      جديد
    </span>
    <img
      class="card-img-top bg-transparent"
      src="@/assets/images/item.png"
      alt=""
    />
    <div class="card-body text-center">
      <p class="card-title h5">اسم المنتج يعرض هنا</p>
      <p class="card-text text-red font-weight-bolder">
        <span>50.00</span><span> ريال</span>
      </p>
      <div class="text-rating">
        <font-awesome-icon icon="star" />
        <font-awesome-icon icon="star" />
        <font-awesome-icon icon="star" />
        <font-awesome-icon icon="star" />
        <font-awesome-icon icon="star" />
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.text-rating {
  color: #d6d249;
}
.text-red {
  color: #66286a;
}
.new {
  width: 50px;
  color: #7be070;
}
.new.border-bottom.border-top {
  border-color: #7be070 !important;
}
.btn-primary {
  background-color: #252525 !important;
}
.category:hover .btn-primary {
  background-color: #66286a !important;
}
</style>
