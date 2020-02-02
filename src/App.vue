<template>
    <v-app id="app">
      <v-navigation-drawer
      color="green"
      dark
      expand-on-hover
      hide-overlay
      permanent
      right
      app
      >
      <v-list
      nav 
      shaped
      dense
      >
        <v-list-item two-line>
          <v-list-item-avatar>
            <img :src="img_adr">
          </v-list-item-avatar>
          <v-divider class="my-3"></v-divider>
          <v-list-item-content class="text-left">
            <v-list-item-title class="font-weight-black">SocialLink</v-list-item-title>
            <v-list-item-subtitle>Name</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
        <v-list-item link :to="path">
          <v-list-item-icon>
            <v-icon>mdi-home-outline</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="text-left">Главная</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item link :to="path">
          <v-list-item-icon>
            <v-icon>mdi-user-outline</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="text-left">Мой профиль</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item link :to="path">
          <v-list-item-icon>
            <v-icon>mdi-adduser-outline</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="text-left">Найти друзей</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
      </v-navigation-drawer>
    
    <v-content class="px-12 py-3">
      <v-container fluid>
        <v-row class="text-left">
            <v-col cols="10">
                <h1 class="green--text text--darken-2">
                    <v-icon large color="green darken-2">mdi-account-outline</v-icon>
                    Иван Иванов
                </h1>
            </v-col>
        </v-row>
        <v-row class="text-left">
            <v-col cols="2">
                <img src="https://randomuser.me/api/portraits/men/7.jpg" style="max-width: 100%">
            </v-col>
            <v-col cols="10" class="text-left">
                <p>
                    Веб-сайт: <a href="..." target="_blank">...</a>
                </p>
                <p>
                    E-mail: <a href="mailto:...">...</a>
                </p>
                <p>
                    Город: ...
                </p>
                <p>
                    Место работы: ...
                </p>
            </v-col>
        </v-row>
        <router-view/>
      </v-container>
    </v-content>

  </v-app>
</template>

<script>
export default {
  
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
