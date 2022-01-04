<!-- eslint-disable vue/no-v-html -->
<template>
  <div class="section-title text-center">
    <h2 class="text-h3 text-md-h2 text-xl-h1 mb-4">{{ title }}</h2>
    <hr class="accent mx-auto" />
    <p
      class="mb-10 mx-auto font-weight-light text-body-2 text-md-body-1"
      style="max-width: 800px"
      v-html="description"
    ></p>
  </div>
</template>

<script>
export default {
  name: 'TitleSection',
  props: {
    title: { type: String, default: () => 'Title', require: true },
    description: { type: String, default: () => '', require: true },
  },
}
</script>

<style lang="scss" scoped>
.section-title {
  hr {
    display: block;
    width: 78px;
    height: 1px;
    margin-top: -2px;
    margin-bottom: 20px;
    clear: both;
    border: 0;
  }
  p {
    letter-spacing: 0 !important;
    line-height: 1.89 !important;
  }
}
</style>
