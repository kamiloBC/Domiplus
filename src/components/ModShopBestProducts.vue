<template>
  <div>
    <v-divider></v-divider>
    <h1
      style="color:grey;"
      class="text-title-mod font-weight-thin ml-4 mt-1 mb-2 mt-3">
      Los mejores productos
    </h1>
    <GridBannerProducts/>
  </div>
</template>

<script>
import GridBannerProducts from '@/components/GridBannerProducts.vue';

export default {
  name: 'ModShopBestProducts',
  components: {
    GridBannerProducts,

  },
};

</script>

<style>
@import '../styles/reset.css';
</style>
