<template>
  <v-card elevation="1">
    <v-row>
      <v-col cols="5" class="pt-0 pb-0">
        <v-img
          src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
          height="100%"
        ></v-img>
      </v-col>
      <v-col cols="7" class="pt-3 pb-0 pl-0">
        <div class="font-weight-medium text--primary pa-0 mb-0">
          Libra de arroz flor huila
        </div>
        <v-row
          class="pb-0"
        >
          <v-col cols="7" class="pb-0 pt-0">
            <v-card-title class="pa-0">
              $ 3.200
            <h5 class="overline ml-1 red--text">
              50%
            </h5>
            <v-card-subtitle class="pa-0 pl-1">
              Envio gratis</v-card-subtitle>
            </v-card-title>
          </v-col>
          <v-col cols="5" class="pb-0 pt-0">
              <v-select
              class="pb-0 mb-0 mr-1"
                :items="items"
                label="1"
                solo
              ></v-select>
          </v-col>
        </v-row>
        <v-card-actions
          class="pt-0"
        >
          <v-btn
            icon
            @click="show = !show"
          >
            <v-icon>mdi-heart</v-icon>
            </v-btn>

          <v-spacer></v-spacer>

            <v-chip
              class=""
              rounded
              outlined
              color="success"
              dark
              v-if="showButtonAdd"
              @click="addAndPay"
            >
              <span class="material-icons ti-1 pr-1">
                shopping_cart
              </span>
                agregar
            </v-chip>
            <v-chip
              rounded
              color="error"
              dark
              outlined
              v-if="showButtonPay"
            >
              <span class="material-icons">
                remove_shopping_cart
              </span>
              quitar
            </v-chip>
        </v-card-actions>
      </v-col>
    </v-row>
  </v-card>
</template>

<script>
export default {
  name: 'HorizontalCardProduct',
  data() {
    return {
      showButtonPay: false,
      showButtonAdd: true,
      items: ['1', '2', '3', '4', '5', '6', '7', '8'],
    };
  },
  methods: {
    addAndPay() {
      this.showButtonPay = true;
      this.showButtonAdd = false;
    },
  },
};
</script>

<style>
.ti-1{
  font-size: 13px;
}
.ti-2{
  font-size: 18px;
}
</style>
