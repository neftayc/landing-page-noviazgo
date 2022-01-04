<template>
  <v-img
    id="home"
    :src="require('@/assets/fondo4.jpg')"
    gradient="to right top, rgba(100,115,201,.2), rgba(0,0,0,.5)"
    width="100%"
    height="100vh"
  >
    <v-container
      id="main-banner"
      class="white--text text-center d-flex flex-column justify-space-between fill-height"
    >
      <div>
        <h1 class="text-h4 py-10 font-weight-medium">Yuli+Rusbel</h1>
        <div class="d-flex align-center justify-center">
          <v-btn
            v-for="item in menus"
            :key="item.to"
            text
            class="item-menu text-white mx-2 white--text text-subtitle-2 text-md-subtitle-1"
            :to="`#${item.to}`"
          >
            {{ item.name }}
          </v-btn>
        </div>
      </div>
      <div class="mb-15 pb-10">
        <div>
          <h2 class="text-h5 text-xl-h4 text-uppercase font-weight-medium">
            BIENVENIDO AL MEJOR DÍA DE NUESTRA VIDA
          </h2>
        </div>
        <div class="main-text">¡Nuestra Boda!</div>
      </div>
    </v-container>
    <img
      style="position: absolute; bottom: 0"
      height="50"
      :src="require('@/assets/slider.png')"
      width="100%"
    />
  </v-img>
</template>

<script>
export default {
  name: 'MainBanner',
  data: () => ({
    menus: [
      { to: 'boda', name: 'Boda' },
      { to: 'nosotros', name: 'Novios' },
      { to: 'galeria', name: 'Galería' },
    ],
  }),
}
</script>

<style lang="scss" scoped>
#main-banner {
  h2 {
    font-family: var(--font-family-two) !important;
    letter-spacing: 0.1em !important;
    display: block;
    margin-bottom: 6px;
    line-height: 1.43 !important;
  }
  .main-text {
    font-size: 7.8rem;
    letter-spacing: 0;
    line-height: 1.1;
    font-family: var(--font-family-one) !important;
    box-sizing: border-box;
  }
  .item-menu {
    font-family: var(--font-family-two) !important;
    font-weight: 600 !important;
  }
}
</style>
