<template>
  <section class="cta">
    <v-container fluid>
      <v-row justify="center">
        <v-col cols="10" sm="8">
          <h2 class="text-center ">
            Få 10 gode råd om
            <br />digital transformation
          </h2>
        </v-col>
        <v-col cols="10" sm="8" class="pt-0">
          <p class="text-center ">
            Ja tak, jeg vil gerne høre mere om digital transformation
          </p>
        </v-col>
        <v-col cols="10" sm="8">
          <v-form ref="form" v-model="valid" lazy-validation>
            <v-container class="text-center">
              <v-row>
                <v-col cols="12" class="py-0">
                  <v-text-field
                    v-model="name"
                    :rules="requiredRule"
                    label="Navn"
                    required
                  ></v-text-field>
                </v-col>
                <v-col cols="12" md="6" class="py-0">
                  <v-text-field
                    v-model="phone"
                    :rules="requiredRule"
                    label="Mobil"
                    required
                  ></v-text-field>
                </v-col>
                <v-col cols="12" md="6" class="py-0">
                  <v-text-field
                    v-model="email"
                    :rules="requiredRule"
                    label="E-mail"
                    required
                  ></v-text-field>
                </v-col>
                <v-col cols="12" md="6" class="py-0">
                  <v-text-field
                    v-model="zipcode"
                    :rules="requiredRule"
                    label="Postnr."
                    required
                  ></v-text-field>
                </v-col>
                <v-col cols="12" md="6" class="py-0">
                  <v-text-field
                    v-model="city"
                    :rules="requiredRule"
                    label="By"
                    required
                  ></v-text-field>
                </v-col>
              </v-row>
              <v-row justify="center">
                <v-col cols="12" sm="6" md="4">
                  <v-btn
                    width="100%"
                    :disabled="!valid"
                    @click="validate"
                    depressed
                    color="white"
                    class="mt-6 cta__submit"
                    x-large
                    >Ring mig op</v-btn
                  >
                </v-col>
              </v-row>
            </v-container>
          </v-form>

          <v-row justify="center">
            <v-col cols="3" sm="2" class="pb-0">
              <Prize />
            </v-col>
            <v-col cols="12" class="text-center pt-0">
              <p>Pentia vinder pris for digital innovation 2017</p>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </section>
</template>
<script>
import Prize from "~/components/images/Prize.vue";
export default {
  components: {
    Prize
  },
  data: () => ({
    valid: true,
    name: "",
    phone: "",
    email: "",
    zipcode: "",
    city: "",
    requiredRule: [v => !!v || "Påkrævet"]
  }),
  methods: {
    validate() {
      this.$refs.form.validate();
    }
  }
};
</script>
<style lang="scss" scoped>
.cta {
  background-color: #eb5b51;
  color: white;
  padding: 75px 0 0 0;

  .cta__submit {
    padding: 1rem;
    color: #eb5b51;
    font-weight: bold;
    text-transform: none;
  }
}
</style>
