<template>
  <v-app>
    <NavigationDrawer
      :drawer = drawer
      @updateDrawer = 'updateDrawer'
    />

    <v-app-bar app>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>Application</v-toolbar-title>
    </v-app-bar>

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
import NavigationDrawer from "@/components/NavigationDrawer.vue"
  export default {
    data: () => ({ drawer: null }),
    components: {
      NavigationDrawer,
    },
    methods: {
      updateDrawer(newValue) {
        this.drawer = newValue
      }
    }
  }
</script>
