<template>
  <v-navigation-drawer
      v-model="drawerComp"
      app
    >
    <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="title">
            BeeManager
          </v-list-item-title>
      </v-list-item-content>
    </v-list-item>

    <v-divider></v-divider>
    <v-list
        dense
        nav
    >
        <v-list-item
            link
            href='Map'
        >
          <v-list-item-icon>
            <v-icon>mdi-call-split</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>Pasieczyska</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
</template>

<script>
  export default {
    name: 'NavigationDrawer',

    data: () => ({

    }),
    computed: {
        drawerComp: {
            get () { return this.drawer },
            set (value) { this.$emit('updateDrawer', value) },    
        }
    },
    props: {
        drawer: null,
    }
  }
</script>