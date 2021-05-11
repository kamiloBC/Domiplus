<template>
  <v-container>
    <v-row>
      <v-col>
        <v-card
          class="mx-auto "
          max-width="300"
          tile
          elevation="0"
        >
          <v-list dense color="#f9f9f9">
            <v-subheader>Domicilio para</v-subheader>
            <v-list-item-group
              v-model="selectedItem"
              color="primary"
            >
              <v-list-item
                v-for="(item, i) in items"
                :key="i"
              >
                <v-list-item-icon>
                  <span
                    v-text="item.icon"
                    class="material-icons">
                  </span>
                </v-list-item-icon>
                <v-list-item-content>
                  <v-list-item-title v-text="item.text"></v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list-item-group>
          </v-list>
        </v-card>
      </v-col>
      <v-col>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    selectedItem: 1,
    items: [
      { text: 'Carlos Perez Agudelo', icon: 'admin_panel_settings' },
      { text: '3114823916', icon: 'call' },
      { text: 'Popayan - Cauca', icon: 'location_city' },
      { text: 'Carrera 39 D Numero 17 -10', icon: 'location_on ' },
    ],
  }),
};
</script>
