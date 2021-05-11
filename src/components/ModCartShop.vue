<template>
  <v-expansion-panels class="pb-4">
    <v-expansion-panel>
      <v-expansion-panel-header v-slot="{ open }">
        <v-row no-gutters
        >
          <v-col cols="4">
            <v-btn
              class="ma-3"
              color="#FA143E"
              fab
              x-small
              dark
            >
              <span class="material-icons">
                shopping_cart
              </span>
            </v-btn>
          </v-col>
          <v-col
            cols="8"
            class="text--secondary pt-4"
          >
            <v-fade-transition leave-absolute>
              <span v-if="open">
                <span class="material-icons red--text">
                  delete_outline
                </span>
                <span class="material-icons green--text ml-9">
                  add_circle_outline
                </span>
                <span class="material-icons ml-9">
                  search
                </span>
              </span>
              <v-row
                v-else
                no-gutters
                style="width: 100%"
              >
                <v-col cols="12"
                  class="container-center-1"
                >
                  <div
                    class="content-center"
                  >
                    <h2>8</h2>
                    <span class="ml-2 pt-1">Domicilios</span>
                  </div>
                </v-col>
                <v-col></v-col>
              </v-row>
            </v-fade-transition>
          </v-col>
        </v-row>
      </v-expansion-panel-header>
      <v-expansion-panel-content>
        <v-card>
          <v-subheader> Programados</v-subheader>
          <v-list-item-group
            v-model="settings"
            multiple
            active-class=""
          >
            <v-list-item>
                <v-list-item-action>
                  <v-checkbox
                    v-model="checkbox"
                ></v-checkbox>
                </v-list-item-action>

                <v-list-item-content>
                  <v-list-item-subtitle>Nombre</v-list-item-subtitle>
                  <v-list-item-title>Contenido</v-list-item-title>
                  <v-list-item-subtitle>Fecha de entrega</v-list-item-subtitle>
                </v-list-item-content>
            </v-list-item>
            <v-list-item>
              <template v-slot:default="{ active }">
                <v-list-item-action>
                  <v-checkbox :input-value="active"></v-checkbox>
                </v-list-item-action>

                <v-list-item-content>
                    <v-list-item-title>Sound</v-list-item-title>
                    <v-list-item-subtitle>Auto-update apps at
                      any time. Data charges may apply</v-list-item-subtitle>
                </v-list-item-content>
              </template>
            </v-list-item>
            <v-list-item>
              <template v-slot:default="{ active }">
                <v-list-item-action>
                  <v-checkbox :input-value="active"></v-checkbox>
                </v-list-item-action>

                <v-list-item-content>
                  <v-list-item-title>Auto-add widgets</v-list-item-title>
                    <v-list-item-subtitle>Automatically
                        add home screen widgets when downloads complete</v-list-item-subtitle>
                    </v-list-item-content>
                  </template>
                </v-list-item>
              </v-list-item-group>
            </v-card>
          <v-card class="mt-2 ">
          <v-subheader>En proceso</v-subheader>
          <v-list-item-group
            v-model="settings"
            multiple
            active-class=""
          >
          <v-list-item>
            <template v-slot:default="{ active }">
              <v-list-item-action>
                <v-checkbox :input-value="active"></v-checkbox>
                  </v-list-item-action>

                  <v-list-item-content>
                  <v-list-item-title>Notifications</v-list-item-title>
                  <v-list-item-subtitle>Notify me about
                  pdates to apps or games that I downloaded</v-list-item-subtitle>
                </v-list-item-content>
              </template>
            </v-list-item>
                  <v-list-item>
                    <template v-slot:default="{ active }">
                      <v-list-item-action>
                        <v-checkbox :input-value="active"></v-checkbox>
                      </v-list-item-action>

                      <v-list-item-content>
                        <v-list-item-title>Sound</v-list-item-title>
                        <v-list-item-subtitle>Auto-update apps at
                        any time. Data charges may apply</v-list-item-subtitle>
                      </v-list-item-content>
                    </template>
                  </v-list-item>

                  <v-list-item>
                    <template v-slot:default="{ active }">
                        <v-list-item-action>
                        <v-checkbox :input-value="active"></v-checkbox>
                      </v-list-item-action>

                      <v-list-item-content>
                        <v-list-item-title>Auto-add widgets</v-list-item-title>
                        <v-list-item-subtitle>Automatically
                        add home screen widgets when downloads complete</v-list-item-subtitle>
                      </v-list-item-content>
                    </template>
                  </v-list-item>
                </v-list-item-group>
              </v-card>
        </v-expansion-panel-content>
      </v-expansion-panel>
    </v-expansion-panels>
</template>
<script>
export default {
  data: () => ({
    settings: [],
    date: null,
    checkbox: true,
    trip: {
      name: '',
      location: null,
      start: null,
      end: null,
    },
    locations: ['Australia', 'Barbados', 'Chile', 'Denmark', 'Ecuador', 'France'],
  }),
};
</script>

<style scoped>

.content-center-1{
  display:flex; flex-direction:row; margin:0 auto;
}

.circle{
  border-radius: 50%;
  background-color: #f20789;
}
</style>
