<template>
    <div>
      <v-app-bar app color="primary" dark>
        <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
        <v-toolbar-title class="white--text">Menú Principal</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn text class="white--text">Solicitudes</v-btn>
        <v-btn text class="white--text">Cerrar Sesión</v-btn>
        <v-btn text class="white--text" @click="showSubMenu = !showSubMenu">Nueva Solicitud</v-btn>
  
        <v-list-item-group v-if="showSubMenu" top="0">
          <v-list-item v-for="item in subMenuItems" :key="item.title" link>
            <v-list-item-icon>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>
            <v-list-item-title class="white--text">{{ item.title }}</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
  
      </v-app-bar>
  
      <v-navigation-drawer app v-model="drawer" color="primary" dark>
        <v-list-item>
          <v-list-item-avatar>
            <v-img src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png" />
          </v-list-item-avatar>
          <v-list-item-title class="title white--text">Vuetify</v-list-item-title>
        </v-list-item>
  
        <v-divider></v-divider>
  
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
    methods: {
      toggleSubMenu() {
        this.showSubMenu = !this.showSubMenu;
      },
    },
  };
  </script>
  
  
  