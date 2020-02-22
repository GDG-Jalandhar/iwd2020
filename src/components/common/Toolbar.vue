<template>
    <v-app-bar
      app
      color="white"
      elevate-on-scroll
    >
      <v-app-bar-nav-icon @click="toggleDrawer"></v-app-bar-nav-icon>

      <v-toolbar-title>IWD Jalandhar 2020</v-toolbar-title>

      <v-spacer></v-spacer>

      <!-- <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn> -->
    </v-app-bar>
</template>

<script>
    import {
        mapGetters,
        mapMutations
    } from 'vuex'
    export default {
        props:{
            color:String
        },
        components:{
        
        },
        computed: {
            ...mapGetters(['links'])
        },
        methods: {
            ...mapMutations(['toggleDrawer']),
            onClick (e, item) {
                e.stopPropagation()
                if (item.to || !item.href) return
                this.$vuetify.goTo(item.href)
            }
        }
    }
</script>