<template>
  <section class="splash">
    <v-container fluid>
      <v-row class="splash__caption">
        <v-col cols="12" style="font-weight: bold">Lorem ipsum</v-col>
      </v-row>
      <v-row justify="center">
        <v-col cols="8" sm="4" md="3">
          <Zeppeliner />
        </v-col>
      </v-row>
      <v-row justify="center">
        <h1>Digital transformation</h1>
      </v-row>
      <v-row justify="center">
        <p>Rådgivning. Implementering. Resultater</p>
      </v-row>
      <v-row justify="center">
        <v-col cols="10" sm="8" md="6">
          <p class="text-center" style="font-size: 0.9rem;">
            Hvordan bliver din virksomhed en digital vinder i fremtiden?
            <br />Hvilke tiltag skal der til strategisk og taktisk for at dreje
            forretningen i den rigtige retning? Hvilke elementer indeholder en
            succesfuld digital transformation? Vi har svarene. Pentia kan hjælpe
            dig på hele rejsen fra strategisk rådgivning til implementering.
          </p>
        </v-col>
      </v-row>
      <v-row justify="center">
        <v-col cols="12">
          <div class="splash__cta" v-scroll-to="'#start-rejse'">
            Start din rejse her
            <v-icon>mdi-dots-vertical</v-icon>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>
<script>
import Zeppeliner from "~/components/images/Zeppeliner.vue";
export default {
  components: { Zeppeliner }
};
</script>
<style lang="scss" scoped>
html {
  scroll-behavior: smooth;
}
.splash {
  padding: 0 12px;
  background-color: #2a2a2c;
  .splash__caption {
    position: absolute;
    font-size: 0.8rem;
    padding: 12px;
  }
  .splash__cta {
    display: grid;
    padding-top: 50px;
    font-size: 0.7rem;
    text-align: center;
    cursor: pointer;
    position: absolute;
    bottom: 12px;
    transform: translateX(-50%);
    left: 50%;
  }
}
</style>
