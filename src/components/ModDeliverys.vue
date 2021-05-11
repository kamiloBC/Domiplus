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
                delivery_dining
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
        <v-list two-line>
          <v-list-item-group
            v-model="selected"
            active-class="pink--text"
            multiple
          >
            <template v-for="(item, index) in items">
              <v-list-item :key="item.title">
                <template v-slot:default="{ active }">
                    <v-icon
                      v-if="!active"
                      color="grey lighten-1"
                    >
                      mdi-star-outline
                    </v-icon>

                    <v-icon
                      v-else
                      color="yellow darken-3"
                    >
                      mdi-star
                    </v-icon>
                  <v-list-item-content>
                    <v-list-item-title v-text="item.title"></v-list-item-title>

                    <v-list-item-subtitle
                      class="text--primary"
                      v-text="item.headline"
                    ></v-list-item-subtitle>

                    <v-list-item-subtitle v-text="item.subtitle"></v-list-item-subtitle>
                  </v-list-item-content>

                  <v-list-item-action>
                    <v-list-item-action-text v-text="item.action"></v-list-item-action-text>
                    <span class="material-icons">
                      check_circle
                    </span>
                  </v-list-item-action>
                </template>
              </v-list-item>

              <v-divider
                v-if="index < items.length - 1"
                :key="index"
              ></v-divider>
            </template>
          </v-list-item-group>
        </v-list>
      </v-expansion-panel-content>
    </v-expansion-panel>
  </v-expansion-panels>
</template>
<script>
export default {
  data: () => ({
    selected: [2],
    items: [
      {
        action: '15 min',
        headline: 'Brunch this weekend?',
        subtitle: `I'll be
         in your neighborhood doing errands this weekend. Do you want to hang out?`,
        title: 'Ali Connors',
      },
      {
        action: '2 hr',
        headline: 'Summer BBQ',
        subtitle: `W
        ish I could come, but I'm out of town this weekend.`,
        title: 'me, Scrott, Jennifer',
      },
      {
        action: '6 hr',
        headline: 'Oui oui',
        subtitle: 'Do you have Paris recommendations? Have you ever been?',
        title: 'Sandra Adams',
      },
      {
        action: '12 hr',
        headline: 'Birthday gift',
        subtitle: 'Have any ideas about what we should get Heidi for her birthday?',
        title: 'Trevor Hansen',
      },
      {
        action: '18hr',
        headline: 'Recipe to try',
        subtitle: 'We should eat this: Grate, Squash, Corn, and tomatillo Tacos.',
        title: 'Britta Holt',
      },
    ],
    settings: [],
    date: null,
    checkbox: false,
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
