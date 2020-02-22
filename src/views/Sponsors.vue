<template>
  <v-content class="px-0 mx-0 pt-1 mt-5">

    <v-container fluid class="pa-0 py-2 mt-5" >
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
