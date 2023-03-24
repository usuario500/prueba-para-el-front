<template>
    <div>
      <v-app-bar app color="primary" dark class="elevation-0">
        <v-img src="https://culiacan.tecnm.mx/wp-content/themes/tecnm/images/logo-tecnm.svg" />
        <v-spacer></v-spacer>
        <v-btn text class="white--text" @click="showSubMenu = !showSubMenu">Nueva Solicitud</v-btn>
        <v-toolbar-title class="white--text">Mantenimiento</v-toolbar-title>
        <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
      </v-app-bar>


  
      <v-list-item-group v-if="showSubMenu" class="sub-menu">
        <v-list-item v-for="item in subMenuItems" :key="item.title" link>
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-title class="white--text">{{ item.title }}</v-list-item-title>
        </v-list-item>
      </v-list-item-group>
  
      <v-navigation-drawer app v-model="drawer" color="blue darken-2"  :right="true" :left="false">
        <v-list-item>
          <v-list-item-avatar>
            <v-img src="https://culiacan.tecnm.mx/wp-content/themes/tecnm/images/logo-itc.svg" />
          </v-list-item-avatar>
          <v-list-item-title class="title white--text">Menu</v-list-item-title>
        </v-list-item>
  
        <v-divider></v-divider>
        <v-btn text class="white--text" @click="showSubMenu = !showSubMenu">Nueva Solicitud</v-btn>
        <v-list dense>
          <v-list-item v-for="item in items" :key="item.title" link>
            <v-list-item-icon>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>
            <v-list-item-title class="white--text">{{ item.title }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-navigation-drawer>
    </div>
  </template>
  
  <style scoped>
  .sub-menu {
  position: absolute;
  top: 60px;
  right: 280px;
  }

  </style>
  
  <script>
  export default {
    data() {
      return {
        drawer: false,
        showSubMenu: false,
        subMenuItems: [
          { title: 'Computo', icon: 'mdi-desktop-mac' },
          { title: 'Mantenimiento', icon: 'mdi-wrench' },
          { title: 'Rec. Materiales', icon: 'mdi-clipboard-plus-outline' },
        ],
        items: [
          { title: 'Solicitudes', icon: 'mdi-note-multiple-outline' },
          { title: 'Cerrar sesión', icon: 'mdi-logout' },
        ],
      };
    },
  };
  </script>
  
  
  