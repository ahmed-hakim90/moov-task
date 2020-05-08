<template>
  <div class="footer mt-5">
    <div class="container">
      <div class="row  border-bottom">
        <div class="col-4 text-light text-right">
          <p class="h3 head-line pb-5">
            نبذة عنا
          </p>
          <p class="pb-2">
            {{ msg }}
          </p>
        </div>
        <div class="col-2 text-light text-right">
          <p class="h3 head-line pb-5">
            نبذة عنا
          </p>
          <ul class="list-group p-0 pb-2">
            <li
              class="list-group-item active bg-transparent rounded-0 border-0"
              v-for="item in list"
              :key="item.index"
            >
              {{ item }}
            </li>
          </ul>
        </div>
        <div class="col-2 text-light text-right">
          <p class="h3 head-line pb-5">
            نبذة عنا
          </p>
          <ul class="list-group p-0 pb-2">
            <li
              class="list-group-item rounded-0 border-0  bg-transparent active"
              v-for="item in list"
              :key="item.index"
            >
              {{ item }}
            </li>
          </ul>
        </div>
        <div class="col-2 text-light text-right ">
          <p class="h3 head-line pb-5">
            نبذة عنا
          </p>

          <ul class="list-group p-0 pb-2  ">
            <li
              class="list-group-item active bg-transparent rounded-0 border-0"
              v-for="item in list"
              :key="item.index"
            >
              {{ item }}
            </li>
          </ul>
        </div>
        <div class="col-2 text-light text-right">
          <p class="h3 head-line pb-5">
            تحميل التطبيق
          </p>
        </div>
      </div>
      <div>
        <p class="m-0 text-center text-light pt-4 pb-2">
          جميع الحقوق محفوظة&copy;
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    msg: `
    الأول كل ملفوظ مفهوم المعنى من الكتاب والسنة سواء كان ظاهرا أو نصا أو مفسرا حقيقة أو مجازا عاما أو خاصا اعتبارا منهم للغالب، لأن عامة ما ورد من صاحب الشرع نصوص، وهذا المعنى هو المراد بالنصوص في قولهم عبارة النص وإشارة النص ودلالة النص واقتضاء النص. فقوله من الكتاب والسنة بيان لقوله ملفوظ،
    `,
    list: [
      "من نحن",
      "منتجاتنا",
      "العلامات التجارية",
      "الشركات التابعة",
      "العروض الخاصة",
      "اسئلة واجوبة",
    ],
  }),
};
</script>

<style lang="scss">
.footer {
  .row {
    padding-top: 100px;
    padding-bottom: 100px;
  }
  background-color: #252525;
  .head-line::after {
    border-color: #66286a !important;
  }
  .list-group {
    .list-group-item {
      padding: 2px;
      transition: all 0.3555s ease-in-out;
      &:hover {
        color: #66286a !important;
      }
    }
  }
}
</style>
