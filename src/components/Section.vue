<template>
  <div class="section mt-4">
    <!-- head-line to bottom ::after after it to draw line bottom -->
    <div class="head-line border-bottom mb-5">
      <p class=" h2  text-right pb-3">
        <!-- 
          here slot is change is you write in it from another place
        if don`t write in it not change
          -->
        <slot name="category-name">
          الكترونيات
        </slot>
      </p>
    </div>
    <div class="row">
      <!-- here put anything you want  -->
      <slot name="item"> </slot>
    </div>
  </div>
</template>

<script>
export default {};
</script>
