<template>
    <div>
      <v-app-bar app color="primary" dark class="elevation-0">
        <v-spacer></v-spacer>
        <v-toolbar-title class="white--text">Mantenimiento</v-toolbar-title>
        <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      </v-app-bar>

      <v-list-item-group v-if="showSubMenu && drawer" class="sub-menu">
        <v-list-item v-for="item in subMenuItems" :key="item.title" link>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-title class="white--text">{{ item.title }}</v-list-item-title>
        </v-list-item>
      </v-list-item-group>
  
      <v-navigation-drawer app v-model="drawer" color="blue darken-2" dark :right="true" :left="false">
        <v-list-item>
          <v-list-item-avatar>
            <v-img src="https://culiacan.tecnm.mx/wp-content/themes/tecnm/images/logo-itc.svg" />
          </v-list-item-avatar>
          <v-list-item-title class="title white--text">Menu</v-list-item-title>
        </v-list-item>
      
        <v-divider></v-divider>
        <v-btn text class="white--text" @click="showSubMenu = !showSubMenu"><v-icon>mdi-file-plus</v-icon>Nueva Solicitud</v-btn>
        <v-list dense>
          <v-list-item v-for="item in items" :key="item.title" link>
            <v-btn text class="white--text"><v-icon>{{ item.icon }}</v-icon><v-list-item-title class="white--text">{{ item.title }}</v-list-item-title></v-btn>
          </v-list-item>
        </v-list>
      </v-navigation-drawer>
    </div>
  </template>
  
  <style scoped>
  .sub-menu {
  position: absolute;
  top: 64px;
  right: 256px;
  z-index: 9999;
  background-color: #fff;
  }

  </style>
  
  <script>
  export default {
    data() {
      return {
        primaryColor: 'blue darken-2',
        drawer: false,
        showSubMenu: false,
        subMenuItems: [
          { title: 'Computo', icon: 'mdi-laptop' },
          { title: 'Mantenimiento', icon: 'mdi-wrench' },
          { title: 'Rec. Materiales', icon: 'mdi-clipboard-plus-outline' },
        ],
        items: [
          { title: 'Solicitudes', icon: 'mdi-note-multiple-outline' },
          { title: 'MTTO preventivo', icon: 'mdi-shield-check-outline' },
          { title: 'Programar MTTO', icon: 'mdi-file-chart-outline' },
          { title: 'Reportes', icon: 'mdi-calendar-month-outline' },
          { title: 'Cerrar sesión', icon: 'mdi-logout' },
        ],
      };
    },
  };
  </script>
  
  
  