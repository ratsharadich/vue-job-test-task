<template>
  <v-app>
    <v-main>
      <ExursionsPage />
    </v-main>
  </v-app>
</template>

<script>
import ExursionsPage from './pages/ExursionsPage.vue';

export default {
  name: 'App',

  components: {
    ExursionsPage,
  },

  data: () => ({
    //
  }),
};
</script>
