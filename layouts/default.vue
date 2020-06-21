<template>
  <v-app>
    <Navigation />
    <v-main>
      <nuxt />
    </v-main>
  </v-app>
</template>

<script>
import Navigation from "~/components/Navigation.vue";
export default {
  components: { Navigation },
  data() {
    return {};
  }
};
</script>

<style lang="scss">
section {
  width: 100%;
  min-height: 100vh;
  position: relative;
}
h1 {
  font-size: 2.5rem;
  font-weight: 900;
}
h2 {
  font-weight: 900;
  line-height: 1.2;
}

::-webkit-scrollbar {
  width: 10px;
}

/* Track */
::-webkit-scrollbar-track {
  background: #d8d8d8;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: #eb5b51;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: #dc483d;
}
</style>
