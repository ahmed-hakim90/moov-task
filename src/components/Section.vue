<template>
  <div class="section mt-4">
    <div class="head-line border-bottom mb-5">
      <p class=" h2  text-right pb-3">
        <slot name="category-name">
          الكترونيات
        </slot>
      </p>
    </div>
    <div class="row">
      <slot name="item"> </slot>
    </div>
  </div>
</template>

<script>

export default {};
</script>

<style lang="scss">
.section {
  .head-line {
    padding-bottom: -5px;
  }
}
</style>
