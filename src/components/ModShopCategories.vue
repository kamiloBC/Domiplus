<template>
  <v-container>
    <v-row justify="center">
      <v-expansion-panels popout
      >
        <v-expansion-panel
          v-for="(item,i) in 5"
          :key="i"
          class="mb-2"
        >
          <v-expansion-panel-header
            class="fondo pb-0 pt-0"
          >
            <h3
            class="white--text Roboto text-categorie font-weight-light"
            >
              Mercado
            </h3>
          </v-expansion-panel-header>
          <v-expansion-panel-content>
            <div>
              <v-row>
                <v-col
                  style="background:blue"
                  cols="6"
                ></v-col>
                <v-col
                  style="background:gray"
                  cols="6"
                ></v-col>
              </v-row>
            </div>
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
    </v-row>
  </v-container>
</template>

<script>
export default {

};

</script>

<style>
.fondo{
  background-image: url("https://picsum.photos/1920/1080?random");
}

.text-categorie{
  font-size: 18px;
  font-style: italic;
  letter-spacing: 1px;
}

</style>
