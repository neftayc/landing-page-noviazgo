<template>
  <v-img
    :src="require('@/assets/fondo3.jpg')"
    height="480"
    position="center left"
    class="align-center"
    gradient="to top right, rgba(0,0,0,.1), rgba(0,0,0,.1)"
  >
    <img
      :src="require('@/assets/slider.png')"
      class="mt-n5"
      width="100%"
      height="130"
      style="transform: rotate(180deg); position: absolute; top: 0"
    />

    <v-carousel
      :continuous="true"
      :cycle="true"
      :show-arrows="false"
      hide-delimiter-background
      delimiter-icon="mdi-minus"
      height="300"
      interval="7000"
      active-class="accent"
    >
      <v-carousel-item
        v-for="(slide, i) in frases"
        :key="i"
        transition="scale-transition"
      >
        <div
          class="text-right text-sm-center fill-height d-flex flex-column justify-center mx-auto px-5"
          style="max-width: 600px; min-width: 250"
        >
          <v-icon color="white" large class="font-weight-light d-block">
            mdi-heart-outline
          </v-icon>
          <div
            class="text-h6 text-sm-h5 text-lg-h4 font-weight-light black--text text--lighten-2 mb-4"
          >
            {{ slide.description }}
          </div>
          <div class="text-caption font-weight-bold mb-10 text-uppercase">
            - {{ slide.autor }} -
          </div>
        </div>
      </v-carousel-item>
    </v-carousel>

    <img
      style="position: absolute; bottom: 0"
      height="100"
      :src="require('@/assets/slider.png')"
      width="100%"
    />
  </v-img>
</template>

<script>
export default {
  name: 'FrasesCelebres',
  data: () => ({
    frases: [
      {
        description: '"Mejor haber amado y perdido que nunca haber amado"',
        autor: 'SAN AGUSTIN',
      },
      {
        description: '"Mi verdadero amor posee mi corazón y yo tengo el suyo"',
        autor: 'PHILIP SIDNEY',
      },
      {
        description: '"El amor no mira con los ojos, sino con el alma"',
        autor: 'william shakespeare',
      },
      {
        description:
          '"Andábamos sin buscarnos, pero sabiendo que andábamos para encontrarnos"',
        autor: 'Cortázar',
      },
    ],
  }),
}
</script>

<style lang="scss" scoped></style>
