<template>
  <v-card
    class="d-flex justify-space-between mx-auto mb-10 grey--text text--lighten-1 rounded-xl transparent elevation-22"
    width="800"
  >
    <div class="text-center px-8 py-6">
      <div class="text-h2 mb-10">{{ contador.dia }}</div>
      <span class="text-h5 text-lg-h4 pb-3 d-block">Day(s)</span>
    </div>
    <v-divider vertical></v-divider>
    <div class="text-center px-8 py-6">
      <div class="text-h2 mb-10">{{ contador.hora }}</div>
      <span class="text-h5 text-lg-h4 pb-3 d-block">Hour(s)</span>
    </div>
    <v-divider vertical></v-divider>
    <div class="text-center px-8 py-6">
      <div class="text-h2 mb-10">{{ contador.min }}</div>
      <span class="text-h5 text-lg-h4 pb-3 d-block">Minute(s)</span>
    </div>
    <v-divider vertical></v-divider>
    <div class="text-center px-8 py-6">
      <div class="text-h2 mb-10">{{ contador.seg }}</div>
      <span class="text-h5 text-lg-h4 pb-3 d-block">Second(s)</span>
    </div>
  </v-card>
</template>

<script>
export default {
  name: 'TheWeddingDay',
  data: () => ({ contador: {} }),
  mounted() {
    setInterval(() => {
      this.contador = this.countDays()
    }, 1000)
  },
  methods: {
    countDays() {
      const second = 1000
      const minute = second * 60
      const hour = minute * 60
      const day = hour * 24
      const countDown = new Date('2022-05-01 0:00:00 AM').getTime()

      const now = new Date().getTime()

      const distance = countDown - now

      const dia = Math.floor(distance / day)
      const hora = Math.floor((distance % day) / hour)
      const min = Math.floor((distance % hour) / minute)
      const seg = Math.floor((distance % minute) / second)
      console.log(seg)

      return { dia, hora, min, seg }
    },
  },
}
</script>

<style lang="scss" scoped></style>
