<template>
      <v-card
        elevation="1"
      >
        <v-img
          src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
          height="150px"
        ></v-img>

        <div class="font-weight-medium text--primary pt-2 pb-0 pl-2">
          Libra de arroz flor huila
        </div>

        <v-card-subtitle
          class="text-decoration-line-through pb-1 pt-0"
        >
          $ 60.000
        </v-card-subtitle>
        <v-card-text class="pb-0 pt-0">
          <v-row>
            <v-col
              cols="7"
              class="pb-0"
            >
              <h4 class="font-weight-medium">
                $ 50.000
              </h4>
              <v-spacer></v-spacer>
              <a class="sizeTextSmall" href="#">Envio gratis</a>
            </v-col>
            <v-col
              cols="5"
              class="pa-0"
            >
              <div class="text-center">
                <v-select
                  :items="items"
                  label="1"
                  solo
                ></v-select>
              </div>
            </v-col>
          </v-row>
        </v-card-text>
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
      </v-card>
</template>

<script>
export default {
  name: 'simpleCartProduct',
  data() {
    return {
      show: false,
      products: [
        {
          id: '1',
          img: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
          name: 'Nombre del producto',
          lastPrice: '$ 60.000',
          Price: '$ 50.000',
          freeSend: true,
          descriptio: 'Esta es la descripcion del producto',
        },
        {
          id: '2',
          img: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
          name: 'Nombre del producto',
          lastPrice: '$ 60.000',
          Price: '$ 50.000',
          freeSend: true,
          descriptio: 'Esta es la descripcion del producto',
        },
        {
          id: '3',
          img: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
          name: 'Nombre del producto',
          lastPrice: '$ 60.000',
          Price: '$ 50.000',
          freeSend: true,
          descriptio: 'Esta es la descripcion del producto',
        },
        {
          id: '4',
          img: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
          name: 'Nombre del producto',
          lastPrice: '$ 60.000',
          Price: '$ 50.000',
          freeSend: true,
          descriptio: 'Esta es la descripcion del producto',
        },
      ],
      items: ['1', '2', '3', '4', '5', '6', '7', '8'],
      showButtonPay: false,
      showButtonAdd: true,
    };
  },
  methods: {
    addAndPay() {
      this.showButtonPay = true;
      this.showButtonAdd = false;
    },
    removeShoppingCard() {
      this.showButtonPay = false;
      this.showButtonAdd = true;
    },
  },
};

</script>

<style>
  .sizeTextSmall{
    font-size: small;
  }

</style>
