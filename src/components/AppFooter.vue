<template>
  <div class="footer mt-5">
    <div class="container">
      <div class="row  border-bottom">
        <div class="col-4 text-light text-right">
          <div>
            <p class="h3 head-line pb-5">
              نبذة عنا
            </p>
            <p class="pb-2">
              {{ msg }}
            </p>
            <p>
              <font-awesome-icon icon="phone-alt" class="ml-2" />
              <span class="phone" dir="ltr">
                997 - 8889 5552 2223 6697
              </span>
              |
              <span class="phone" dir="ltr">
                997 - 8889 5552 2223 6697
              </span>
            </p>
            <p>
              <font-awesome-icon icon="envelope" class="ml-2" />
              <span class="phone" dir="ltr">
                Admin@domainname.com
              </span>
            </p>
            <div class="list-group list-group-horizontal">
              <button
                type="button"
                class="list-group-item list-group-item-action rounded-0 border-0 text-center"
                v-for="(icon, index) in icons"
                :key="index"
              >
                <font-awesome-icon :icon="['fab', icon]" />
              </button>
            </div>
          </div>
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
              class="list-group-item rounded-0 border-0  bg-transparent "
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
          <img src="@/assets/images/Untitled.png" class="w-100" />
        </div>
      </div>
      <div>
        <p class="m-0 text-center text-light pt-4 pb-2">
          {{ copyRight }} &copy;
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    active: undefined,
    msg: `
    الأول كل ملفوظ مفهوم المعنى من الكتاب والسنة سواء كان ظاهرا أو نصا أو مفسرا حقيقة أو مجازا عاما أو خاصا اعتبارا منهم للغالب، لأن عامة ما ورد من صاحب الشرع نصوص، وهذا المعنى هو المراد بالنصوص في قولهم عبارة النص وإشارة النص ودلالة النص واقتضاء النص. فقوله من الكتاب والسنة بيان لقوله ملفوظ،
    `,
    copyRight: "  جميع الحقوق محفوظة لستور موف 2020",
    list: [
      "من نحن",
      "منتجاتنا",
      "العلامات التجارية",
      "الشركات التابعة",
      "العروض الخاصة",
      "اسئلة واجوبة",
    ],
    icons: ["instagram", "facebook-f", "twitter", "snapchat"],
  }),
};
</script>
