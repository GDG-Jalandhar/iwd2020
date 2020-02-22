<template>
    <v-app-bar
      app
      fixed
      elevate-on-scroll
    >
      <v-app-bar-nav-icon @click="toggleDrawer"></v-app-bar-nav-icon>

      <v-toolbar-title class="google-font">IWD Jalandhar 2020</v-toolbar-title>

      <v-spacer></v-spacer>

        <!-- <v-btn
            v-for="(link, i) in links"
            :key="i"
            :to="link.to"
            
            class="ml-0 google-font hidden-sm-and-down"
            style="text-transform: capitalize;" 
            text
            @click="onClick($event, link)"
        >
            {{ link.text }}
        </v-btn> -->
        <v-btn text router-link to="home" class="hidden-sm-and-down">
            Home
        </v-btn>

        <v-btn text router-link to="team" class="hidden-sm-and-down">
            Team
        </v-btn>

        <v-btn icon v-on:click="darkMode" class="ml-2">
            <v-icon v-if="this.$vuetify.theme.dark">mdi-brightness-7</v-icon>
            <v-icon v-else>mdi-brightness-4</v-icon>
        </v-btn>

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
            },

            darkMode(){
                let metaThemeColor = document.querySelector("meta[name=theme-color]");
                this.$vuetify.theme.dark = !this.$vuetify.theme.dark
                if(localStorage)
                    localStorage.setItem('darkMode',this.$vuetify.theme.dark);
                if(this.$vuetify.theme.dark){
                metaThemeColor.setAttribute("content", '#212121');
                }else{
                metaThemeColor.setAttribute("content", '#f5f5f5');
                }
            }
        }
    }
</script>