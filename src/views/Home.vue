<template>
  <div style="width:100%; background:#f9f9f9; padding-top:230px;"
  >
    <SimpleBanner/>
    <ModMainNumContact/>
    <v-container fluid
    >
      <v-row>
        <v-col cols="12" sm="6">
          <ModMainChat/>
        </v-col>
        <v-col cols="12" sm="6">
          <ModMainServices/>
        </v-col>
      </v-row>
    </v-container>
    <ModMainShop/>
    <ModShopOnlyToday/>
    <ModShopSale/>
    <MainFooter/>
  </div>
</template>

<script>
// @ is an alias to /src
import ModMainNumContact from '@/components/ModMainNumContact.vue';
import ModMainChat from '@/components/ModMainChat.vue';
import ModMainServices from '@/components/ModMainServices.vue';
import ModMainShop from '@/components/ModMainShop.vue';
import ModShopOnlyToday from '@/components/ModShopOnlyToday.vue';
import ModShopSale from '@/components/ModShopSale.vue';
import MainFooter from '@/components/MainFooter.vue';
import SimpleBanner from '../components/SimpleBanner.vue';

export default {
  name: 'Home',
  components: {
    ModMainNumContact,
    ModMainChat,
    ModMainServices,
    ModMainShop,
    ModShopOnlyToday,
    ModShopSale,
    MainFooter,
    SimpleBanner,
  },
  data: () => ({
    SimpleBanner,
    loading: false,
    search: '',
    selected: [],
  }),

  computed: {
    botonService() {
      return this.iconservices;
    },
    allSelected() {
      return this.selected.length === this.items.length;
    },
    categories() {
      const search = this.search.toLowerCase();

      if (!search) return this.items;

      return this.items.filter((item) => {
        const text = item.text.toLowerCase();

        return text.indexOf(search) > -1;
      });
    },
    selections() {
      const selections = [];

      for (const selection of this.selected) {
        selections.push(selection);
      }
      return selections;
    },
  },

  watch: {
    selected() {
      this.search = '';
    },
  },

  methods: {
    next() {
      this.loading = true;

      setTimeout(() => {
        this.search = '';
        this.selected = [];
        this.loading = false;
      }, 2000);
    },
  },
};
</script>

<style>
</style>
