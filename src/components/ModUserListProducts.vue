<template>
  <v-expansion-panels>
    <v-expansion-panel>
      <v-expansion-panel-header v-slot="{ open }">
        <v-row no-gutters
        >
          <v-col cols="4">
            <v-btn
              color="#FA143E"
              fab
              x-small
              dark
            >
              <span class="material-icons">
                delivery_dining
              </span>
            </v-btn>
          </v-col>
          <v-col
            cols="8"
            class="text--secondary pt-2"
          >
            <v-fade-transition leave-absolute>
              <span v-if="open">
                <span class="material-icons ml-1 red--text">
                  delete_outline
                </span>
                <span class="material-icons ml-6">
                  add_shopping_cart
                </span>
                <span class="material-icons ml-6">
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
                    <h2>28</h2>
                    <span class="ml-2 pt-1">Productos</span>
                  </div>
                </v-col>
                <v-col></v-col>
              </v-row>
            </v-fade-transition>
          </v-col>
        </v-row>
      </v-expansion-panel-header>
      <v-expansion-panel-content>
        <v-row
          justify="space-around"
          no-gutters
        >
          <v-col cols="3">
            <v-menu
              ref="startMenu"
              :close-on-content-click="false"
              :return-value.sync="trip.start"
              offset-y
              min-width="290px"
            >
              <template v-slot:activator="{ on, attrs }">
                <v-text-field
                  v-model="trip.start"
                  label="Start date"
                  prepend-icon="mdi-calendar"
                  readonly
                  v-bind="attrs"
                  v-on="on"
                ></v-text-field>
              </template>
              <v-date-picker
                v-model="date"
                no-title
                scrollable
              >
                <v-spacer></v-spacer>
                <v-btn
                  text
                  color="primary"
                  @click="$refs.startMenu.isActive = false"
                >
                  Cancel
                </v-btn>
                <v-btn
                  text
                  color="primary"
                  @click="$refs.startMenu.save(date)"
                >
                  OK
                </v-btn>
              </v-date-picker>
            </v-menu>
          </v-col>

          <v-col cols="3">
            <v-menu
              ref="endMenu"
              :close-on-content-click="false"
              :return-value.sync="trip.end"
              offset-y
              min-width="290px"
            >
              <template v-slot:activator="{ on, attrs }">
                <v-text-field
                  v-model="trip.end"
                  label="End date"
                  prepend-icon="mdi-calendar"
                  readonly
                  v-bind="attrs"
                  v-on="on"
                ></v-text-field>
              </template>
              <v-date-picker
                v-model="date"
                no-title
                scrollable
              >
                <v-spacer></v-spacer>
                <v-btn
                  text
                  color="primary"
                  @click="$refs.endMenu.isActive = false"
                >
                  Cancel
                </v-btn>
                <v-btn
                  text
                  color="primary"
                  @click="$refs.endMenu.save(date)"
                >
                  OK
                </v-btn>
              </v-date-picker>
            </v-menu>
          </v-col>
        </v-row>
      </v-expansion-panel-content>
    </v-expansion-panel>
  </v-expansion-panels>
</template>
<script>
export default {
  data: () => ({
    date: null,
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
