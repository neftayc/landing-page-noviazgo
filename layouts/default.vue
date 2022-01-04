<template>
  <v-app dark>
    <Banner />
    <v-main>
      <Nuxt />
    </v-main>
    <footer class="mt-5">
      <div class="text-center white--text" style="overflow: hidden">
        <img
          :src="require('@/assets/slider.png')"
          class="d-block mt-n1"
          width="100%"
          height="200"
          style="transform: rotate(180deg); background-color: #3b3b3b"
        />
        <div
          style="background-color: #3b3b3b"
          class="accent--text text--lighten-3 text-h3 pt-5 pb-1"
        >
          Yuli+Rusbel
          <p
            class="text-subtitle-2 pt-3 mb-10 grey--text mb-15 font-weight-light"
          >
            Estamos Enamorados y casándonos
          </p>
          <p class="text-caption pt-3 mb-2 grey--text">
            ©Copyright. Todos los derechos reservados
          </p>
        </div>
      </div>
    </footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
}
</script>
