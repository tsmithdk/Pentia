<template>
  <div class="navigation">
    <v-navigation-drawer
      v-model="sidebarMenu"
      app
      floating
      mini-variant
      permanent
      color="#1B1B1D"
    >
      <v-list dense dark>
        <v-list-item>
          <v-list-item-action>
            <nuxt-link to="/">
              <img class="logo" src="/logo.svg" alt="Pentia" />
            </nuxt-link>
          </v-list-item-action>
        </v-list-item>
      </v-list>
      <v-list-item class="btnMenu" @click="overlayMenu = !overlayMenu">
        <v-icon>{{ overlayMenu ? "mdi-close" : "mdi-menu" }}</v-icon>
      </v-list-item>
    </v-navigation-drawer>
    <v-overlay :value="overlayMenu" opacity="1">
      <v-list rounded nav color="rgba(255, 0, 0, 0)">
        <v-list-item-group v-model="item">
          <v-list-item
            v-for="(item, i) in items"
            :key="i"
            @click="overlayMenu = false"
            :to="item.link"
          >
            <v-list-item-content
              v-if="item.text"
              :style="{ 'justify-content': 'center' }"
              >{{ item.text }}</v-list-item-content
            >
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-overlay>
  </div>
</template>

<script>
export default {
  data() {
    return {
      sidebarMenu: true,
      overlayMenu: false,

      title: "Vuetify.js",
      item: 0,
      items: [
        { text: "HJEM", link: "/" },
        { text: "CASES", link: "/cases" },
        { text: "SERVICES", link: "/services" },
        { text: "KARRIERE", link: "/karriere" },
        { text: "NYT", link: "/nyt" },
        { text: "EVENT", link: "/event" },
        { text: "OM PENTIA", link: "/om-pentia" }
      ]
    };
  }
};
</script>

<style lang="scss">
.logo {
  width: 100%;
  height: 34px;
  filter: brightness(0) invert(1);
}
.btnMenu {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
}
</style>
