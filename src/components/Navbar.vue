<template>
  <v-app-bar app dark color="#323B50" flat>
    <v-tabs color="#F34F64">
      <v-tabs-slider color="#F34F64"> </v-tabs-slider>
      <v-tab class="withoutupercase">Camisa</v-tab>
      <v-tab class="withoutupercase">Zapatos</v-tab>
      <v-tab class="withoutupercase">Chaquetas</v-tab>
      <v-tab class="withoutupercase">Sombreros</v-tab>
      <v-tab class="withoutupercase">Pantalones</v-tab>
    </v-tabs>
    <v-btn small color="#F34F64">
      <v-icon>mdi-chevron-down</v-icon>
    </v-btn>
    <v-spacer></v-spacer>
    <v-divider vertical inset class="mr-4"></v-divider>
    <v-text-field label="Buscar" prepend-inner-icon="mdi-magnify" dense class="mt-4"></v-text-field>
    <v-btn text small class="withoutupercase grey--text">
      Hola, Cristian
      <v-icon small>mdi-chevron-down</v-icon>
    </v-btn>
  </v-app-bar>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      links: ["Dashboard", "Messages", "Profile", "Updates"],
      items: [{ icon: "mdi-laptop" }, { icon: "mdi-tag-outline" }, { icon: "mdi-shopping-outline" }, { icon: "mdi-wallet-travel" }, { icon: "mdi-apps" }, { icon: "mdi-text-box-multiple-outline" }],
    };
  },
};
</script>

<style>
.v-tabs-slider {
  position: absolute;
  top: 30%;
  left: 50%;
  transform: translate(-50%, -50%);
  height: 15px !important;
  width: 20px !important;
  border-radius: 150px 150px 0px 0px;
  background-color: #f34f64;
}
.v-tab.withoutupercase {
  text-transform: none !important;
}

.v-tabs {
  width: 30% !important;
}

.v-btn:not(.v-vbtn--round).v-size--small {
  min-width: 10px !important;
  padding: 0 5px !important;
}

.theme--dark.v-text-field > .v-input__control > .v-input__slot:before {
  border-color: #323b50 !important;
}
</style>
