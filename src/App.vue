<template>
  <v-app>
    <Toolbar/>
    <Drawer/>

    <v-content>
      <HelloWorld/>
    </v-content>
  </v-app>
</template>

<script>
import Toolbar from './components/common/Toolbar'
import Drawer from './components/common/Drawer'
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    HelloWorld,
    Toolbar,
    Drawer
  },

  data: () => ({
    //
  }),
};
</script>
