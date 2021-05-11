<template>
  <div>
    <v-divider></v-divider>
    <h1
      style="color:grey;"
      class="text-title-mod font-weight-thin ml-4 mt-1 mb-2 mt-3">
      Lo mejor para tu despensa
    </h1>
    <SimpleCarousel/>
    <GridSimpleProducts/>
    <GridHorizontalProducts/>
  </div>
</template>

<script>
import SimpleCarousel from '@/components/SimpleCarousel.vue';
import GridSimpleProducts from '@/components/GridSimpleProducts.vue';
import GridHorizontalProducts from '@/components/GridHorizontalProducts.vue';

export default {
  name: 'ModShopFoods',
  components: {
    SimpleCarousel,
    GridSimpleProducts,
    GridHorizontalProducts,
  },

};

</script>
