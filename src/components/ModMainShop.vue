<template>
  <div>
    <div>
      <v-divider></v-divider>
      <h1
       class="Roboto text-title-mod font-weight-thin ml-4 mt-1 mb-3">Descubre para ti</h1>
    </div>
    <v-carousel
      cycle
      height="400"
      hide-delimiter-background
      delimiter-icon="mdi-minus"
      show-arrows-on-hover
    >
      <v-carousel-item
        v-for="(slide, i) in slides"
        :key="i"
      >
        <v-sheet
          :color="colors[i]"
          height="100%"
        >
          <v-row
            class="fill-height"
            align="center"
            justify="center"
          >
            <div class="display-3">
              {{ slide }} Slide
            </div>
          </v-row>
        </v-sheet>
      </v-carousel-item>
    </v-carousel>
    <GridBannerProducts/>
    <GridHorizontalProducts/>

  </div>
</template>

<script>
import GridBannerProducts from '@/components/GridBannerProducts.vue';
import GridHorizontalProducts from '@/components/GridHorizontalProducts.vue';

export default {
  name: 'ModMainShop',
  components: {
    GridBannerProducts,
    GridHorizontalProducts,
  },
  data() {
    return {
      colors: [
        'indigo',
        'warning',
        'pink darken-2',
        'red lighten-1',
        'deep-purple accent-4',
      ],
      slides: [
        'First',
        'Second',
        'Third',
        'Fourth',
        'Fifth',
      ],
    };
  },
};
</script>

<style>
  .text-size{
    font-size: 1rem;
  }

  .text-title-mod {
  font-size: 1.3rem;
  letter-spacing: 1px;
}
@media (max-width: 800px) {
    .text-title-mod {
      font-size: 2rem;
    }
  }

</style>
