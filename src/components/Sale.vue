<template>
  <div class="sale mt-4  ">
    <div
      class="position-absolute sale-bottom-side d-flex align-items-center text-right pt-4 pr-4"
    >
 <!-- container-content  haven`t style    -->
      <div class="container-content">
        <p class="h6">
          <slot name="category-name">
            اكسسورات
          </slot>
        </p>
        <p class="h1 head-line">خصم %{{ discount }}</p>
      </div>
    </div>
    <slot name="image-item-sale"></slot>
  </div>
</template>

<script>
export default {
  props: ["discount"],
};
</script>

<style lang="scss">
.sale {
  position: relative;
  .sale-bottom-side {
    bottom: 0;
    right: 0;
    left: 0;
    height: 150px;
    background-color: #ffffff87;
    transition: all 0.355s ease-in-out;
  }
  &:hover .sale-bottom-side {
    height: 100%;
  }
}
</style>
