<template>
  <div>
    <section id="boda" class="mb-10 mt-n2">
      <v-responsive :aspect-ratio="16 / 4" min-height="600">
        <v-img
          :src="require('@/assets/fondo1.webp')"
          class="align-center"
          height="100%"
        >
          <img
            :src="require('@/assets/slider.png')"
            width="100%"
            height="100"
            style="
              transform: rotate(180deg);
              position: absolute;
              top: 0;
              z-index: 1;
            "
          />
          <TitleSection
            title="El 01 de Mayo del 2022"
            description="En el Centro Poblado Sunchubamba, Paucartambo <br> Cusco"
          />
          <Days />
          <img
            style="position: absolute; bottom: 0"
            height="150"
            :src="require('@/assets/slider.png')"
            width="100%"
          />
        </v-img>
      </v-responsive>
    </section>
    <v-img :src="require('@/assets/fondo2.webp')" position="center center">
      <section id="nosotros" class="py-15">
        <TitleSection
          title="¡Conozca al Futuro Sr. y Sra. Ccana!"
          description="Y ahora permanecen la fe, la esperanza y el amor, estos tres; pero el mayor de ellos es el amor. ¡Cómo decidimos que deberíamos estar juntos para siempre!"
        />
        <Novios />
      </section>
    </v-img>
    <section id="tarjetaInvitacion" class="pb-15">
      <div style="height: 560px; position: relative">
        <img
          :src="require('@/assets/slider.png')"
          width="100%"
          height="200"
          style="
            transform: rotate(180deg);
            position: absolute;
            top: 0;
            z-index: 1;
          "
        />
        <Invite />
        <img
          style="position: absolute; bottom: 0"
          height="200"
          :src="require('@/assets/slider.png')"
          width="100%"
        />
      </div>
    </section>
    <section id="galeria" class="py-15">
      <TitleSection
        title="Galeria"
        description="!Nuestros momentos hermosos e inolvidables!"
      />
      <Gallery />
    </section>
    <section id="frasesCelebres">
      <Frases />
    </section>
    <section id="map" class="py-15">
      <TitleSection
        title="Nuestra Ubicación"
        description="En el Centro Poblado Sunchubamba, Paucartambo <br> Cusco"
      />
      <div>
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m28!1m8!1m3!1d234407.3274317279!2d-71.87389556088596!3d-13.449134416500636!3m2!1i1024!2i768!4f13.1!4m17!3e0!4m5!1s0x916dd5d826598431%3A0x2aa996cc2318315d!2sCusco!3m2!1d-13.53195!2d-71.96746259999999!4m5!1s0x916e698b3f0e0c1b%3A0xbde51c7d0d0bd999!2sPaucartambo!3m2!1d-13.3140102!2d-71.5931657!4m3!3m2!1d-13.2635841!2d-71.62121619999999!5e0!3m2!1ses-419!2spe!4v1640294017446!5m2!1ses-419!2spe"
          width="100%"
          height="450"
          style="border: 0"
          allowfullscreen=""
          loading="lazy"
        ></iframe>
      </div>
    </section>
  </div>
</template>

<script>
import TitleSection from '~/components/UI/TitleSection.vue'
export default {
  name: 'IndexPage',
  components: { TitleSection },
}
</script>

<style lang="scss" scoped></style>
