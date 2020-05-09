<template>
  <div class="sale mt-4  ">
    <div
      class="position-absolute sale-bottom-side d-flex align-items-center text-right pt-4 pr-4"
    >
      <!-- container-content  haven`t style    -->
      <div class="container-content">
        <p class="h6">
          <!-- 
            here is slot write anything you want on it from any place
           -->
          <slot name="category-name">
            اكسسورات
          </slot>
        </p>
        <!-- 
          discount is come from palce render component
          discount prop is required with componentI
         -->
        <p class="h1 head-line">خصم %{{ discount }}</p>
      </div>
    </div>
    <!-- 

      here slot you can make it anything
     -->
    <slot name="image-item-sale"></slot>
  </div>
</template>

<script>
export default {
  props: {
    discount: {
      require: true
    }
  }
};
</script>

<style lang="scss"></style>
