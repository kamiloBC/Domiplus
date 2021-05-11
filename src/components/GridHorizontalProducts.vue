<template>
<v-container fluid>
  <v-row>
    <v-col
      v-for="n in 6"
      :key="n"
      class="d-flex child-flex pa-1"
      cols="12"
      sm="4"
    >
      <HorizontalCardProduct/>
    </v-col>
  </v-row>
</v-container>
</template>

<script>
import HorizontalCardProduct from '@/components/HorizontalCardProduct.vue';

export default {
  name: 'GridHorizontalProducts',
  components: {
    HorizontalCardProduct,
  },
};
</script>
