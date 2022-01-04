<template>
  <v-responsive :aspect-ratio="16 / 9" height="100%">
    <video
      id="video-play"
      loop
      muted
      autoplay
      width="100%"
      height="100%"
      :poster="require('@/assets/banner.jpg')"
    >
      <source :src="require('@/assets/invitacion.mp4')" type="video/mp4" />
    </video>
  </v-responsive>
</template>

<script>
export default {
  name: 'CardInvite',
}
</script>

<style lang="scss" scoped>
video {
  background: transparent;
  object-fit: cover;
}
</style>
