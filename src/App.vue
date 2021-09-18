<template>
  <v-app id="inspire">
    <v-navigation-drawer
      v-model="drawer"
      app
    >
      <!-- crear un componente que va a tener todo el contenido de mi barra de navegación -->
  <Menubarraizquierda :title="title" :isAdmin="true"/>
    </v-navigation-drawer>

    <v-app-bar app>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>{{title}}</v-toolbar-title>
    </v-app-bar>

    <v-main>
      <!--  -->
    </v-main>
  </v-app>
</template>

<script>
import Menubarraizquierda from './components/Menubarraizquierda.vue';

export default {
  name: "App",
  components: {
    Menubarraizquierda
  },

  data (){
    //mostrar o no la barra modifica el componente drawer barra lado izquierdo
   return{
     title:"Aprendizaje Siglo XXI",
   drawer: false
   }
  }
};
</script>
