<template>
  <v-app>
    <Toolbar/>
    <Drawer/>

    <ViewData/>
  </v-app>
</template>

<script>
import Toolbar from './components/common/Toolbar'
import Drawer from './components/common/Drawer'
import ViewData from './components/common/View'
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    Toolbar,
    Drawer,
    ViewData
  },

  data: () => ({
    //
  }),
};
</script>
