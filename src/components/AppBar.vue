<template>
  <div class="border-bottom">
    <div class="container">
      <nav class="  row ">
        <div class="nav col pr-0 justify-content-start">
          <a class="nav-link" href="#">
            توصيل سريع يصل الي 3 ساعات
          </a>

          <a class="nav-link" href="#">
            شحن مجاني للطلبات بقيمة 50 ريال
          </a>
        </div>

        <div class="nav col justify-content-end">
          <a class="nav-link " href="#">
            تسجيل
          </a>

          <a class="nav-link" href="#">
            تسجيل الدخول
          </a>

          <a class="nav-link active" href="#"> البيع علي منصة موف ستور </a>
          <!-- here intaractive lang switch if you wants -->
          <select class="bg-transparent border-0" v-model="selected">
            <option value="EN">EN</option>
            <option value="AR">AR</option>
            <option value="GR">GR</option>
          </select>
        </div>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    selected: "EN",
  }),
};
</script>
