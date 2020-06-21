<template>
  <v-layout column justify-center align-center>
    <Splash />
    <ValueProposition id="start-rejse" />
    <Cta />
  </v-layout>
</template>

<script>
import Splash from "~/components/Splash.vue";
import ValueProposition from "~/components/ValueProposition.vue";
import Cta from "~/components/Cta.vue";

export default {
  components: {
    Splash,
    ValueProposition,
    Cta
  },
  head: {
    title: "Pentia | Konsulenthus",
    meta: [
      {
        hid: "description",
        name: "description",
        content:
          "Pentia er et uafhængigt digitalt konsulenthus fyldt med nytænkende strateger, designere og udviklere."
      }
    ]
  }
};
</script>
