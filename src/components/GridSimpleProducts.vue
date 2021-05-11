<template>
<v-container fluid>
  <v-row>
    <v-col
      v-for="n in 8"
      :key="n"
      class="d-flex child-flex pa-1"
      cols="6"
      sm="3"
    >
      <SimpleCardProduct/>
    </v-col>
  </v-row>
</v-container>
</template>

<script>
import SimpleCardProduct from '@/components/SimpleCardProduct.vue';

export default {
  name: 'GridBannerProducts',
  components: {
    SimpleCardProduct,
  },
};
</script>
