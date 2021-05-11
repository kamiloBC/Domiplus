<template>
  <div style="width:100%; background:#f9f9f9; padding-top:230px;">
     <v-container fluid>
        <v-row>
           <v-col cols="12" sm="6" class=" pt-0">
            <ModDeliverys/>
            <ModUserListProducts/>
          </v-col>
           <v-col cols="12" sm="6" class="pt-5">
            <ModCartShop/>
            <ModFavoriteProducts/>
           </v-col>
        </v-row>
     </v-container>
  </div>
</template>
<script>

// @ is an alias to /src
import ModDeliverys from '@/components/ModDeliverys.vue';
import ModCartShop from '@/components/ModCartShop.vue';
import ModUserListProducts from '@/components/ModUserListProducts.vue';
import ModFavoriteProducts from '@/components/ModFavoriteProducts.vue';

export default {
  name: 'User',
  components: {
    ModDeliverys,
    ModCartShop,
    ModFavoriteProducts,
    ModUserListProducts,
  },
};
</script>
