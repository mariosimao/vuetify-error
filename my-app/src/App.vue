<template>
  <v-app>
    <my-sidebar/>
  </v-app>
</template>

<script>
// eslint-disable-next-line import/no-extraneous-dependencies
import MySidebar from 'my-lib/src/components/MySidebar.vue';

export default {
  name: 'App',
  components: {
    MySidebar,
  },
};
</script>
