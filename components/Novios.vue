<template>
  <v-container class="py-10">
    <v-row>
      <v-col cols="12" sm="6" order="1">
        <v-img
          class="rounded-xs mx-auto"
          height="460"
          :src="require('@/assets/novia.jpeg')"
          max-width="80%"
        ></v-img>
      </v-col>
      <v-col cols="12" sm="6" order="1">
        <v-card
          class="pa-8 d-flex flex-column justify-space-between fill-height text-center transparent"
          flat
          tile
        >
          <div class="novios-title">
            <h2 class="text-h3">Rusbel Ccana</h2>
            <hr class="accent mx-auto my-6" />
            <span>Escrito por la Novia</span>
          </div>
          <p class="novios-text text-body-2 text-md-body-1 font-weight-light">
            Rusbel es mi amigo más antiguo. Es encantador, responsable,
            extravagante, amante de Dios y sincero, todo en uno solo. Me
            presentaron a esta increíble persona por primera vez en la
            iglesia...
          </p>
          <div>
            <v-btn class="mx-2" fab small color="#fecdd0" dark depressed>
              <v-icon>mdi-facebook</v-icon>
            </v-btn>
            <v-btn class="mx-2" fab small color="#fecdd0" dark depressed>
              <v-icon>mdi-twitter</v-icon>
            </v-btn>
            <v-btn class="mx-2" fab small color="#fecdd0" dark depressed>
              <v-icon>mdi-instagram</v-icon>
            </v-btn>
          </div>
        </v-card>
      </v-col>
    </v-row>
    <v-row class="mt-15 pt-15">
      <v-col cols="12" sm="6" order="4" class="text-center">
        <v-img
          class="rounded-xs"
          height="460"
          :src="require('@/assets/novio.jpg')"
          max-width="80%"
        ></v-img>
      </v-col>
      <v-col cols="12" sm="6" order="3">
        <v-card
          class="pa-8 d-flex flex-column justify-space-between fill-height text-center transparent"
          flat
          tile
        >
          <div class="novios-title">
            <h2 class="text-h3">Yuli Florez</h2>
            <hr class="mx-auto my-6" />
            <span>Escrito por el Novio</span>
          </div>
          <p class="novios-text text-body-2 text-md-body-1 font-weight-light">
            Yuli es la persona más dulce del mundo, aunque aveces también puede
            resultar intimidante. Me dice que aun no conosco esa parte de ella,
            solo espero nunca hacerlo...
          </p>
          <div>
            <v-btn class="mx-2" fab small color="#fecdd0" dark depressed>
              <v-icon>mdi-facebook</v-icon>
            </v-btn>
            <v-btn class="mx-2" fab small color="#fecdd0" dark depressed>
              <v-icon>mdi-twitter</v-icon>
            </v-btn>
            <v-btn class="mx-2" fab small color="#fecdd0" dark depressed>
              <v-icon>mdi-instagram</v-icon>
            </v-btn>
          </div>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'SectionNovios',
}
</script>

<style lang="scss" scoped>
.novios-title {
  hr {
    display: block;
    width: 78px;
    height: 1px;
    clear: both;
    border: 0;
    background: var(--v-accent-base);
  }
  span {
    font-family: var(--font-family-two);
    font-style: normal;
    font-weight: 300;
    font-size: 28px;
    line-height: 1.43;
    letter-spacing: 0.1em;
    color: #58626c;
  }
}
.novios-text {
  letter-spacing: 0 !important;
  line-height: 1.89 !important;
}
</style>
