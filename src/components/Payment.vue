<template>
  <v-card flat class="card_item pa-2 mt-2" elevation="2">
    <v-list subheader two-line color="transparent">
      <v-list-item>
        <v-list-item-avatar size="50px">
          <v-icon class="blue-grey darken-2" color="#737e97" dark>mdi-account-outline</v-icon>
        </v-list-item-avatar>
        <v-list-item-content>
          <v-list-item-title class="white--text">Cliente</v-list-item-title>
          <v-list-item-subtitle class="grey--text mt">Click aquí para agregar cliente</v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>
    </v-list>
    <v-tabs color="#f34f64" v-model="tab1" background-color="transparent" class="order" dark grow>
      <v-tabs-slider color="#f34F64"></v-tabs-slider>
      <v-tab class="withoutupercase">Orden acual</v-tab>
      <v-tab class="withoutupercase">pedidos en espera</v-tab>
    </v-tabs>
    <v-divider color="#3f495e" class="divider_tab"></v-divider>
    <v-tabs-items v-model="tab1">
      <v-tab-item>
        <v-list subheader two-line color="#323b50">
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title class="white--text subtitle-2">Brown Casual Shoes</v-list-item-title>
              <v-list-item-subtitle class="grey--text mt-2">Shoes</v-list-item-subtitle>
            </v-list-item-content>
            <v-list-item-content>
              <v-list-item-subtitle class="grey--text ml-10"> </v-list-item-subtitle>
            </v-list-item-content>
            <v-list-item-action>
              <v-list-item-title class="white--text subtitle-2">$87</v-list-item-title>
            </v-list-item-action>
          </v-list-item>
          <!--Hoodie kece  -->
          <v-divider color="#3f495e" class="divider_tab"></v-divider>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title class="white--text subitle-2">Hoodie Kece</v-list-item-title>
              <v-list-item-subtitle class="grey--text mt-2">Jacket</v-list-item-subtitle>
            </v-list-item-content>
            <v-list-item-content>
              <v-list-item-subtitle class="grey--text mt-2">2</v-list-item-subtitle>
            </v-list-item-content>
            <v-list-item-action>
              <v-list-item-title class="white--text subitle-2">$107</v-list-item-title>
            </v-list-item-action>
          </v-list-item>
          <!-- grey parka -->
          <v-divider color="#3f495e" class="divider_tab"></v-divider>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-title class="white--text subitle-2">Grey Parka Cool</v-list-item-title>
              <v-list-item-subtitle class="grey--text mt-2">Jacket</v-list-item-subtitle>
            </v-list-item-content>
            <v-list-item-content>
              <v-list-item-subtitle class="grey--text mt-2">2</v-list-item-subtitle>
            </v-list-item-content>
            <v-list-item-action>
              <v-list-item-title class="white--text subitle-2">$107</v-list-item-title>
            </v-list-item-action>
          </v-list-item>
          <!-- descuento -->
          <v-divider color="#3f495e" class="divider_tab"></v-divider>
          <v-list-item>
            <v-list-item-content>
              <v-list-item-subtitle class="grey--text mt-2">Discount</v-list-item-subtitle>
              <v-list-item-title class="white--text subitle-2">Total</v-list-item-title>
            </v-list-item-content>
            <v-list-item-action>
              <v-list-item-subtitle class="orange--text">-$2</v-list-item-subtitle>
              <v-list-item-title class="green--text subtitle mt-2">$185</v-list-item-title>
            </v-list-item-action>
          </v-list-item>
          <!-- buttons -->
          <v-divider color="#f495e" class="divider_tab"></v-divider>
          <div class="text-right mt-6 mb-6">
            <v-btn text color="#f34f64" class="withoutupercase">Borrar</v-btn>
            <v-btn color="#f34f64" dark rounded class="withoutupercase">Verificar</v-btn>
          </div>
        </v-list>
      </v-tab-item>
    </v-tabs-items>
  </v-card>
</template>

<script>
export default {
  name: "Payment",
  data() {
    return {
      tab1: null,
    };
  },
};
</script>

<style scoped>
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
  width: 50% !important;
}
.v-tabs.order {
  width: 100% !important;
}
.theme--light.v-card.card_item {
  background-color: #323b50 !important;
  color: #babec9;
}

.v-sheet.v-card.card_item {
  border-radius: 0px !important;
}

.v-divider.divider_tab {
  height: 2px !important;
  max-height: 2px !important;
}

.v-btn.withoutupercase {
  text-transform: none !important;
}
</style>
>
