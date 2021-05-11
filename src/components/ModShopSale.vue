<template>
  <div>
    <div>
      <v-divider></v-divider>
      <h1
        style="color:grey;"
        class="text-title-mod font-weight-thin ml-4 mt-1 mb-2 mt-3">Más Promociones
      </h1>
    </div>
    <v-img
      class="pa-0"
      lazy-src="https://picsum.photos/id/11/10/6"
      max-height="100"
      max-width="100%"
      src="https://picsum.photos/id/11/500/300"
    ></v-img>
    <GridSimpleProducts/>
  </div>
</template>

<script>
import GridSimpleProducts from '@/components/GridSimpleProducts.vue';

export default {
  name: 'ModShopSale',
  components: {
    GridSimpleProducts,
  },
};

</script>

<style>

</style>
