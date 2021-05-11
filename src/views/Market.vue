<template>
  <div style="width:100%; background:#f9f9f9; padding-top:220px;"
  >
  <SimpleBanner/>
  <v-container fluid>
    <v-row>
      <v-col
        cols="12"
        sm="7"
        class="pt-0 pb-0 pl-0 pr-0"
      >
        <ModShopCategories/>
      </v-col>
      <v-col
        cols="12"
        sm="5"
        class="pl-1 pr-1"
      >
        <GridBannerProducts/>
      </v-col>
    </v-row>
    </v-container>
    <ModShopFoods/>
    <ModShopBestProducts/>
    <ModShopSale/>
    <MainFooter/>
  </div>
</template>

<script>
// @ is an alias to /src
import ModShopCategories from '@/components/ModShopCategories.vue';
import SimpleBanner from '@/components/SimpleBanner.vue';
import GridBannerProducts from '@/components/GridBannerProducts.vue';
import ModShopFoods from '@/components/ModShopFoods.vue';
import ModShopBestProducts from '@/components/ModShopBestProducts.vue';
import ModShopSale from '@/components/ModShopSale.vue';
import MainFooter from '@/components/MainFooter.vue';

export default {
  name: 'Market',
  components: {
    ModShopCategories,
    SimpleBanner,
    GridBannerProducts,
    ModShopFoods,
    ModShopBestProducts,
    ModShopSale,
    MainFooter,
  },
};
</script>

<style>

</style>
