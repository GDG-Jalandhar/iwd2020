<template>
  <v-content class="px-0 mx-0 pt-1">
    <v-container fluid class="px-0 pt-5 mt-5" >
      <v-row justify="center" align="center" class="py-3 pa-2" :class="this.$vuetify.theme.dark == true?'black':'grey lighten-4'" >
        <v-col md="12" sm="12" lg="7" cols="12" xs="12" class="pt-3 pa-5"  >
          <img src="https://www.womentechmakers.com/static/images/wtm-icon.png" alt="" srcset="">
          <h1 class="google-font">International Women's Day 2020 Celebration</h1>
          <p class="google-font">International Women's Day (IWD) is marked on March 8th every year. In different regions, the focus of celebrations ranges from general respect and appreciation for women to a celebration of women's economic, political, and social achievements.</p>
          <p class="google-font">#GDGJalandhar &nbsp;&nbsp;&nbsp;&nbsp;  #WTMJalandhar &nbsp;&nbsp;  #GDG  &nbsp;&nbsp; #WTM  &nbsp;&nbsp; #WTM20 &nbsp;&nbsp;  #IWD20 &nbsp;&nbsp;   #IWDJalandhar  </p>

          <h3 class="google-font">Coming Soon...</h3>

        </v-col>
        <v-col md="12" lg="3" xs="12" class="pt-3 pa-5"  >
         
        </v-col>
      </v-row>
    </v-container>

    <v-container fluid class="px-0 pt-5 mt-5" >
      <v-row justify="center" align="center" class="py-3" >
        <v-col md="12" lg="7" xs="12" cols="12" class="pt-3 pa-5"   >
          <div :class="$vuetify.theme.dark == true?'darkModeCard':'whiteTheme'" class="pa-5" >
            <p class="google-font">Theme</p>
            <h1 class="google-font">Together We Rise</h1>
            <p class="google-font">This International Women's Day, we’re inviting our community to share their superpowers - those special qualities that make you shine. Whether you’re creating space for more voices to be heard or you’re working to secure funding as an entrepreneur, you’re a superhero in our book. Together let’s celebrate the super-women in our lives. Together let’s create a new narrative for our industry. 
            #TogetherWeRise.</p>
          </div>
          
        </v-col>
        <v-col md="12" lg="3" xs="12" class="pt-3 pa-5"  >
         
        </v-col>
      </v-row>
    </v-container>

    <v-container fluid class="pa-0 py-2" >
      <v-row justify="center" align="center">
        <v-col md="12" lg="10" xs="12" class="py-0">
          <partners />
        </v-col>
      </v-row>
    </v-container>



  </v-content>
</template>

<script>
import partners from '../components/common/partners'
export default {
  components: {
    partners
  },
  created(){
    let metaThemeColor = document.querySelector("meta[name=theme-color]");
    if(this.$vuetify.theme.dark){
      metaThemeColor.setAttribute("content", '#212121');
    }else{
        metaThemeColor.setAttribute("content", '#f5f5f5');
    }
  }
};
</script>

<style scoped>
  .whiteTheme{
    background: white;
    border:1px solid #e0e0e0;
    border-radius:5px
  }
</style>
