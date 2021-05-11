<template>
  <v-container fluid>
    <v-divider></v-divider>
    <h1
       style="color:grey;"
       class="text-title-mod font-weight-thin ml-4 mt-1 mb-2 mt-3">Solo Hoy</h1>
    <v-row>
      <v-col
        class="pa-1"
        cols="12"
        sm="7"
      >
        <SimpleCarousel/>
      </v-col>
      <v-col
        class="pa-1"
        cols="12"
        sm="5"
      >
        <FeaturedProductCart/>
      </v-col>
    </v-row>
    <v-row>
      <v-col class="pa-0"
      >
        <GridSimpleProducts/>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import FeaturedProductCart from '@/components/FeaturedProductCart.vue';
import SimpleCarousel from '@/components/SimpleCarousel.vue';
import GridSimpleProducts from '@/components/GridSimpleProducts.vue';

export default {
  name: 'ModShopOnlyDay',
  components: {
    FeaturedProductCart,
    SimpleCarousel,
    GridSimpleProducts,
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
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: .5;
  position: absolute;
  width: 100%;
}
/* Mediaqueries Desktop Screen*/
@media (min-width: 800px) {
  .v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: .5;
  position: absolute;
  width: 100%;
  }

}
</style>
