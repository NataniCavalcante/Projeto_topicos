<template>
  <v-card
    class="mx-auto overflow-hidden"
    height="400"
  >
    <v-app>
      <v-app-bar
        app
        dark
        color="green"
        elevation="4"
        
      >
        Menu
        <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>
        <v-toolbar-title>{{ $route.name }}</v-toolbar-title>
      </v-app-bar>
      <v-navigation-drawer
        v-model="drawer"
        absolute
        temporary
      >
        <v-list nav dense>
          <v-list-item-group
            v-model="group"
            active-class="red--text text--accent-4"
          >
            <v-list-item to="/contador">
              <v-list-item-icon>
                <v-icon>mdi-sync</v-icon>
              </v-list-item-icon>
              <v-list-item-title>Contador</v-list-item-title>
            </v-list-item>
            <v-list-item to="/noticias">
              <v-list-item-icon>
                <v-icon>mdi-newspaper</v-icon>
              </v-list-item-icon>
              <v-list-item-title>Notícias</v-list-item-title>
            </v-list-item>
            <v-list-item to="/produtos">
              <v-list-item-icon>
                <v-icon>mdi-gift</v-icon>
              </v-list-item-icon>
              <v-list-item-title>Produtos</v-list-item-title>
            </v-list-item>
             <v-list-item to="/contato">
              <v-list-item-icon>
                <v-icon>mdi-phone</v-icon>
              </v-list-item-icon>
              <v-list-item-title>contato</v-list-item-title>
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </v-navigation-drawer>
      <v-main>
        <v-container fill-height>
          <router-view />
        </v-container>
      </v-main>
      <template>
        <v-treeview
          rounded
          hoverable
          activatable
          :items="items"
        ></v-treeview>
      </template>
    </v-app>
  </v-card>
</template>

<script>
  export default {
    data: () => ({
      drawer: false,
      group: null,
    }),
  }
  
</script>
  

<style scoped>

</style>