<template>
  <v-app>

    <v-app-bar app color="primary" dark>
  <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

  <v-toolbar-title>The Blessings of Surah Ar Rahman</v-toolbar-title>
</v-app-bar>

    <v-card>
  <v-navigation-drawer app  v-model="drawer">

<v-list-item>
  <v-list-item-content>
    <v-list-item-title>Table of Content</v-list-item-title>
  </v-list-item-content>
</v-list-item>

<v-divider></v-divider>

    <v-list>
  <v-list-item
    v-for="(item, index) in menus"
    :key="`menu-`+index"
    :to="item.route"
  >
    <v-list-item-icon>
      <v-icon left>{{ item.icon }}</v-icon>
    </v-list-item-icon>

    <v-list-item-content>
      <v-list-item-title>{{ item.title }}</v-list-item-title>
    </v-list-item-content>
  </v-list-item>
</v-list>


<template v-slot:append>
        <div class="pa-2">
          <h6> &copy; {{ new Date().getFullYear() }} — <strong>Cendolicious</strong></h6>
        </div>
</template>
  </v-navigation-drawer>
</v-card>

    <v-content>
      <v-container fluid>

        <router-view></router-view>
      </v-container>
    </v-content>

    <v-footer absolute app>
    <v-card-text class="text-center">
      &copy; {{ new Date().getFullYear() }} — <strong>Cendolicious</strong>
    </v-card-text>
  </v-footer>

  </v-app>
</template>
<script>
export default {
  name: 'App',
  data: () => ({
    drawer: false,
    menus: [
    { title: 'Home', icon: 'mdi-home', route: '/' },
    { title: 'Prolog', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 1', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 2', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 3', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 4', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 5', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 6', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 7', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 8', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 9', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 10', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 11', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 12', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 13', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 14', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 15', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 17', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 19', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 20', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 22', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 24', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 26', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 27', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 29', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 31', icon: 'mdi-bookmark', route: '/about' }, 
    { title: 'Ayat 33', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 35', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 37', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 38', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 39', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 40', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 41', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 42', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 43', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 44', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 45', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 46', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 47', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 48', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 49', icon: 'mdi-bookmark', route: '/about' },
    { title: 'Ayat 50', icon: 'mdi-bookmark', route: '/about' }
  ], 
  })
}
</script>