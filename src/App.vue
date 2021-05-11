<template>
  <v-app
    >
      <v-card
      >
        <v-app-bar
          absolute
          color="#FA143E"
          dark
          shrink-on-scroll
          prominent
          src="https://picsum.photos/1920/1080?random"
          fade-img-on-scroll
          scroll-target="#scrolling-techniques-3"
        >
          <template v-slot:img="{ props }">
            <v-img
              v-bind="props"
              gradient="to top right, rgba(255,115,201,.7), rgba(255,32,72,.7)"
            ></v-img>
          </template>

          <v-toolbar-title class="Roboto text-logo">
          <img src="../public/img/icons/logorapicilios.png" alt="rapi" class="logo-rapicilios">
          Domiplus</v-toolbar-title>

          <v-spacer></v-spacer>

          <v-btn icon>
            <v-icon>mdi-magnify</v-icon>
          </v-btn>

          <v-btn icon>
            <span class="material-icons">location_on</span>
          </v-btn>

          <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

          <template v-slot:extension>
            <v-tabs align-with-title>
              <v-tab><router-link to="/">
              <span style="color:white;" class="material-icons">home</span>
              </router-link></v-tab>
              <v-tab><router-link to="/market">
              <span style="color:white;" class="material-icons">store</span>
              </router-link></v-tab>
              <v-tab><router-link to="/user">
              <span style="color:white;" class="material-icons">person</span>
              </router-link></v-tab>
              <v-tab><router-link to="/user">
              <span style="color:white;" class="material-icons">chat</span>
              </router-link></v-tab>
              </v-tabs>
          </template>
        </v-app-bar>
        <v-sheet
          id="scrolling-techniques-3"
          class="overflow-y-auto"
          max-height="800"
        >
          <div>
            <router-view/>
          </div>
        </v-sheet>
      </v-card>
          <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
    >
      <v-list-item>
        <v-list-item-avatar>
          <v-img src="https://randomuser.me/api/portraits/men/78.jpg"></v-img>
        </v-list-item-avatar>

        <v-list-item-content>
          <v-list-item-title>John Leider</v-list-item-title>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list dense>
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </v-app>
</template>

<script>
import { mdiAccount } from '@mdi/js';

export default {
  name: 'App',

  components: {
  },

  data: () => ({
    drawer: null,
    icons: {
      svgPath: mdiAccount,
    },
    group: null,
  }),
  waatch: {
    group() {
      this.drawer = false;
    },
  },
};
</script>

<style>
html {
  overflow: hidden;
}
.white-color {
 color: white;
}
.logo-rapicilios{
  height: 25px;
  width: 45px;
  color: #6A76AB;
}
.text-logo {
  font-size: 30px;
  font-style: italic;
  letter-spacing: 1px;
}
#icon-user {
  color: white;
  height: 32px;
  widows: 32px;
}

/*Mediaqueries movil landscape*/
@media (orientation: landscape) {

}

/*Mediaqueries Tablets Screen*/
@media screen and (min-width: 768px) {

}

/* Mediaqueries Desktop Screen*/
@media (min-width: 1200px) {
  *{overflow: hidden;}
  .logo-rapicilios{
    height: 25px;
    width: 45px;
    color: #6A76AB;
  }
  .text-logo {
    font-size: 30px;
    font-style: italic;
    letter-spacing: 1px;
  }
}
</style>
