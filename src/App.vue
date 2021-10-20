<template>
  <v-app>
    <v-app-bar
      ><!---->
      <v-app-bar>
        <v-app-bar-nav-icon></v-app-bar-nav-icon>Mi App<!--hamburguesa-->
        <v-spacer></v-spacer
        ><!--propiedades flex de css separa a la derecha-->
        <v-toolbar-items class="hidden-sm-and-down"
          ><!-- agrupa a los elementos de navegación-->
          <v-btn text>Inicio</v-btn>
          <v-btn text>Buscar</v-btn>
          <v-btn text>Acerca de</v-btn>
        </v-toolbar-items>
      </v-app-bar>
    </v-app-bar>

    <v-container class="fill-height" fluid style="min-height: 434px">
      <v-fade-transition mode="out-in">
        <v-row class="row px-16">
          <v-col cols="4" v-for = "(item, index) in personajes" :key = "index">
            <v-card>
              <v-img
                :src="item.imagen"
                height="420"
                class="grey darken-4"
              ></v-img>
              <v-card-title class="text-h6"> {{ item.nombre }} </v-card-title>
            </v-card>
          </v-col>          
        </v-row>
      </v-fade-transition>
    </v-container>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data() {
    return {
      personajes: [
      { // si tiene linter decirle q fixed all, para q saque las comillas a las key de este json y convierte a un objeto, acá está como json(con comillas)
      'id': 1,
      'nombre': 'Morty',
      'imagen':
      'https://rickandmortyapi.com/api/character/avatar/2.jpeg'
      },
      {
      'id': 2,
      'nombre': 'Rick',
      'imagen':
      'https://rickandmortyapi.com/api/character/avatar/1.jpeg'
      },
      {
      'id': 3,
      'nombre': 'Summer',
      'imagen':
      'https://rickandmortyapi.com/api/character/avatar/3.jpeg'
      },
      {
      'id': 4,
      'nombre': 'Beth',
      'imagen':
      'https://rickandmortyapi.com/api/character/avatar/4.jpeg'
      },
      {
      'id': 5,
      'nombre': 'Jerry',
      'imagen':
      'https://rickandmortyapi.com/api/character/avatar/5.jpeg'
      }
      ]
    }
  }
};
</script>
