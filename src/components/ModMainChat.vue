<template>
        <v-card
          class="mx-auto"
        >
          <v-toolbar
            flat
            color="transparent"
          >
            <v-toolbar-title>¿Que necesitas..?</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn
              icon
            >
              <v-img
                lazy-src="../assets/img/icon-instagram.svg"
                max-height="20"
                max-width="20"
                src="../assets/img/icon-instagram.svg"
                class="mt-1 mr-1"
              ></v-img>
            </v-btn>
            <v-btn
              icon
            >
              <v-img
                lazy-src="../assets/img/icon-facebook-circle.svg"
                max-height="20"
                max-width="20"
                src="../assets/img/icon-facebook-circle.svg"
                class="mt-1 mr-1"
              ></v-img>
            </v-btn>
            <v-btn
              icon
            >
              <span style="" class="material-icons">settings_voice</span>
            </v-btn>
          </v-toolbar>

          <v-container class="py-0">
            <v-row
              align="center"
              justify="start"
            >
              <v-col
                v-for="(selection, i) in selections"
                :key="selection.text"
                class="shrink"
              >
                <v-chip
                  :disabled="loading"
                  close
                  @click:close="selected.splice(i, 1)"
                >
                  <v-icon
                    left
                    v-text="selection.icon"
                  ></v-icon>
                  {{ selection.text }}
                </v-chip>
              </v-col>

              <v-col
                v-if="!allSelected"
                cols="12"
              >
                <v-text-field
                  ref="search"
                  v-model="search"
                  full-width
                  hide-details
                  label="Search"
                  single-line
                ></v-text-field>
              </v-col>
            </v-row>
          </v-container>

          <v-divider v-if="!allSelected"></v-divider>

          <v-list>
            <template v-for="item in categories">
              <v-list-item
                v-if="!selected.includes(item)"
                :key="item.text"
                :disabled="loading"
                @click="selected.push(item)"
              >
                <v-list-item-avatar>
                  <v-icon
                    :disabled="loading"
                    v-text="item.icon"
                  ></v-icon>
                </v-list-item-avatar>
                <v-list-item-title v-text="item.text"></v-list-item-title>
              </v-list-item>
            </template>
          </v-list>

          <v-divider></v-divider>

          <v-card-actions>
            <v-spacer></v-spacer>
             <v-btn
               :disabled="!selected.length"
               :loading="loading"
               color="purple"
               text
               @click="next"
            >
                Next
             </v-btn>
          </v-card-actions>
        </v-card>
</template>

<script>
export default {
  name: 'ModMainChat',
  components: {
  },
  data: () => ({
    items: [
      {
        text: 'Nature',
        icon: 'mdi-nature',
      },
      {
        text: 'Nightlife',
        icon: 'mdi-glass-wine',
      },
      {
        text: 'November',
        icon: 'mdi-calendar-range',
      },
      {
        text: 'Portland',
        icon: 'mdi-map-marker',
      },
      {
        text: 'Biking',
        icon: 'mdi-bike',
      },
    ],
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
.img-service{
  text-align: center;
}
.name-service{
  margin-top: 0.5rem;
  font-size: 0.6rem;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande',
  'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  font-weight: 500;
}
</style>
