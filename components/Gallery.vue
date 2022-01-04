<template>
  <v-container class="px-0">
    <v-row>
      <v-col
        v-for="(item, i) in imagenes"
        :key="item.id"
        class="d-flex child-flex"
        cols="4"
      >
        <v-hover v-slot="{ hover }">
          <v-card flat tile :class="{ 'on-hover': hover }">
            <v-img
              :src="item.image"
              :lazy-src="`https://picsum.photos/10/6?image=${i * 5 + 10}`"
              aspect-ratio="1"
              class="grey lighten-2"
            >
              <template #placeholder>
                <v-row class="fill-height ma-0" align="center" justify="center">
                  <v-progress-circular
                    indeterminate
                    color="grey lighten-5"
                  ></v-progress-circular>
                </v-row>
              </template>
              <v-expand-transition transition="fade-transition">
                <v-card
                  v-if="hover"
                  color="rgba(254, 205, 208, 0.70)"
                  flat
                  tile
                  class="fade-transition d-flex align-center justify-center pointer"
                  style="height: 100%; cursor: pointer"
                  @click="view(item)"
                >
                  <v-icon color="white" class="text-h3 font-weight-light"
                    >mdi-plus</v-icon
                  >
                </v-card>
              </v-expand-transition>
            </v-img>
          </v-card>
        </v-hover>
      </v-col>
    </v-row>
    <v-row>
      <v-dialog
        v-model="viewImage"
        max-width="600"
        overlay-opacity="0.9"
        overlay-color="black"
      >
        <v-card height="80vh" class="transparent">
          <v-img
            height="100%"
            class="rounded-lg"
            contain
            :src="imageSelected.image"
          ></v-img>
        </v-card>
      </v-dialog>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'OurGallery',
  data: () => ({
    viewImage: false,
    imageSelected: require('@/assets/gallery/1.jpg'),
    imagenes: [
      { id: 1, image: require('@/assets/gallery/1.jpg') },
      { id: 2, image: require('@/assets/gallery/2.jpg') },
      { id: 3, image: require('@/assets/gallery/3.jpg') },
      { id: 4, image: require('@/assets/gallery/4.jpg') },
      { id: 5, image: require('@/assets/gallery/5.jpg') },
      { id: 6, image: require('@/assets/gallery/6.jpg') },
    ],
  }),
  methods: {
    view(item) {
      this.viewImage = true
      this.imageSelected = item
    },
  },
}
</script>

<style lang="scss" scoped></style>
