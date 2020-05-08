<template>
  <div class="banner">
    <div class="container-fluid">
      <div class="row">
        <!-- 
          this is highly featrues for us  
          for loop on array cards 
          to show it
         -->
        <div class="col-4" v-for="card in cards" :key="card.index">
          <!-- tis is built card featrue  for everyone -->
          <div
            class="card-before-banner text-light  d-flex align-items-center justify-content-center "
          >
          <!-- here icon for card -->
            <font-awesome-icon :icon="['fab', card.icon]" class="ml-4" />
            <!-- here is text for featrue -->
            <span>
              {{ card.title }}
            </span>
          </div>
        </div>
      </div>
    </div>
    <!-- this is image Banner after featrues -->
    <img :src="imgBanner" class="w-100" />

  </div>
</template>

<script>
import banner from "@/assets/images/Untitled.png";
export default {
  data: () => ({
    // for render image to show it in banner
    imgBanner: banner,
    //  belonges for featrues section
    cards: [
      {
        title: "  دفع امن 100%",
        icon: "cc-visa",
      },
      {
        title: "  دفع امن 100%",
        icon: "cc-visa",
      },
      {
        title: "  دفع امن 100%",
        icon: "cc-visa",
      },
    ],
  }),
};
</script>

<style>
.card-before-banner {
  /* margin:-15px ; */
  height: 80px;
  background-color: #a580a7;
  margin-bottom: 20px;
  font-size: 20px;
}
.col-4:last-of-type {
  padding-left: 0;
}
</style>
