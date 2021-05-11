<template>
  <v-row>
    <v-col
      class="container-center"
      cols="6"
    >
      <div
      class="content-center"
      >
        <v-img
          lazy-src="../assets/img/icon-phone.svg"
          max-height="20"
          max-width="20"
          src="../assets/img/icon-phone.svg"
          class="mt-1 mr-3"
        ></v-img>
        <div>
          <a><h1 class="local-numbers">(034)45456</h1></a>
        </div>
      </div>
    </v-col>
    <v-col
      class="container-center"
      cols="6"
    >
      <div
        class="content-center"
      >
        <v-img
          lazy-src="../assets/img/icon-whatsapp.svg"
          max-height="20"
          max-width="20"
          src="../assets/img/icon-whatsapp.svg"
          class="mt-1 mr-3"
        ></v-img>
        <div>
          <a><h1 class="local-numbers">311481223</h1></a>
          <a><h1 class="local-numbers">311481223</h1></a>
        </div>
      </div>
    </v-col>
  </v-row>
</template>
<style>
.local-numbers {
  color: grey;
  font: Roboto;
  font-weight: 400;
  font-size: 1.2rem;
  font-style: italic;
  letter-spacing: 0.1rem;
}
.container-center{
  display:flex; align-items: center;
}
.content-center{
  display:flex; flex-direction:row; margin:0 auto;
}
/* Mediaqueries Desktop Screen*/
@media (min-width: 1200px) {
  .local-numbers {
    color: grey;
    font: Roboto;
    font-weight: 400;
    font-size: 1.3rem;
    font-style: italic;
  }
}
</style>
