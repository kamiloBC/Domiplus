<template>
  <v-card
    elevation="0"
    color="#f9f9f9"
  >
    <v-row>
      <v-col
        cols="4"
        sm="3"
        v-for="item in iconservices" :key="item.id"
      >
        <div
          class="text-center"
          style="justify-content:center; align-items:center;"
        >
          <v-avatar
            size="70"
          >
            <img
              class="img-service"
              :src="item.img"
              alt="John"
            >
          </v-avatar>
          <h1 class="name-service">{{item.name}}</h1>
        </div>
      </v-col>
    </v-row>
  </v-card>
</template>

<script>

export default {
  name: 'ModMainServices',
  data: () => ({
    iconservices: [
      {
        id: '1',
        img: 'https://cdn.vuetifyjs.com/images/john.jpg',
        name: 'HOTELES',
      },
      {
        id: '2',
        img: 'https://cdn.vuetifyjs.com/images/john.jpg',
        name: 'HOTELES',
      },
      {
        id: '3',
        img: 'https://cdn.vuetifyjs.com/images/john.jpg',
        name: 'HOTELES',
      },
      {
        id: '4',
        img: 'https://cdn.vuetifyjs.com/images/john.jpg',
        name: 'HOTELES',
      },
      {
        id: '5',
        img: 'https://cdn.vuetifyjs.com/images/john.jpg',
        name: 'HOTELES',
      },
      {
        id: '6',
        img: 'https://cdn.vuetifyjs.com/images/john.jpg',
        name: 'HOTELES',
      },
      {
        id: '7',
        img: 'https://cdn.vuetifyjs.com/images/john.jpg',
        name: 'HOTELES',
      },
      {
        id: '8',
        img: 'https://cdn.vuetifyjs.com/images/john.jpg',
        name: 'HOTELES',
      },
    ],
  }),
};

</script>
