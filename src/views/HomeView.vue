<template>
  <v-app :style="{ background: $vuetify.theme.themes.dark.background }">
    <Sidebar />
    <Navbar />
    <v-container fluid>
      <v-app-bar dark color="transparent" flat>
        <v-tabs color="#F34F64" v-model="tab">
          <v-tabs-slider color="#F34F64"></v-tabs-slider>
          <v-tab class="withoutupercase">Paracaidas</v-tab>
          <v-tab class="withoutupercase">Parka</v-tab>
          <v-tab class="withoutupercase">Steve</v-tab>
          <v-tab class="withoutupercase">Dennis</v-tab>
        </v-tabs>
      </v-app-bar>
      <v-card tile color="#323b50" class="my-2 card_global">
        <v-row>
          <v-col cols="12" sm="8">
            <v-tabs-items v-model="tab">
              <!-- paracaidas -->
              <v-tab-item>
                <v-card flat class="card_item pa-2">
                  <v-row>
                    <v-col cols="12" sm="3" v-for="(parasut, index) in parasuts" :key="index">
                      <v-hover v-slot="{ hover }" close-delay="200">
                        <v-card :elevation="hover ? 16 : 2" :class="{ 'on-hover': hover }" class="mx-auto" height="250" tile color="#333c51" align="center">
                          <v-card-actions>
                            <v-spacer></v-spacer>
                            <v-btn tile small :color="hover ? '#F34F64' : '#777d8b'" dark>
                              {{ parasut.prix }}
                            </v-btn>
                          </v-card-actions>
                          <v-img :src="parasut.avatar" width="150" height="150"></v-img>
                          <v-card-text :class="hover ? 'red--text' : 'white--text'">{{ parasut.title }}</v-card-text>
                        </v-card>
                      </v-hover>
                    </v-col>
                  </v-row>
                </v-card>
              </v-tab-item>
              <!-- Parkas -->
              <v-tab-item>
                <v-card flat class="card_item pa-2">
                  <v-row>
                    <v-col cols="12" sm="3" v-for="(parka, index) in parkas" :key="index">
                      <v-hover v-slot="{ hover }" close-delay="200">
                        <v-card :elevation="hover ? 16 : 2" :class="{ 'on-hover': hover }" class="mx-auto" height="250" tile color="#333c51" align="center">
                          <v-card-actions>
                            <v-spacer></v-spacer>
                            <v-btn tile small :color="hover ? '#F34F64' : '#777d8b'" dark>
                              {{ parka.prix }}
                            </v-btn>
                          </v-card-actions>
                          <v-img :src="parka.avatar" width="150" height="150"></v-img>
                          <v-card-text :class="hover ? 'red--text' : 'white--text'">{{ parka.title }}</v-card-text>
                        </v-card>
                      </v-hover>
                    </v-col>
                  </v-row>
                </v-card>
              </v-tab-item>

              <!-- Steves -->
              <v-tab-item>
                <v-card flat class="card_item pa-2">
                  <v-row>
                    <v-col cols="12" sm="3" v-for="(steve, index) in steves" :key="index">
                      <v-hover v-slot="{ hover }" close-delay="200">
                        <v-card :elevation="hover ? 16 : 2" :class="{ 'on-hover': hover }" class="mx-auto" height="250" tile color="#333c51" align="center">
                          <v-card-actions>
                            <v-spacer></v-spacer>
                            <v-btn tile small :color="hover ? '#F34F64' : '#777d8b'" dark>
                              {{ steve.prix }}
                            </v-btn>
                          </v-card-actions>
                          <v-img :src="steve.avatar" width="150" height="150"></v-img>
                          <v-card-text :class="hover ? 'red--text' : 'white--text'">{{ steve.title }}</v-card-text>
                        </v-card>
                      </v-hover>
                    </v-col>
                  </v-row>
                </v-card>
              </v-tab-item>

              <!-- Dennis -->
              <v-tab-item>
                <v-card flat class="card_item pa-2">
                  <v-row>
                    <v-col cols="12" sm="3" v-for="(denni, index) in dennis" :key="index">
                      <v-hover v-slot="{ hover }" close-delay="200">
                        <v-card :elevation="hover ? 16 : 2" :class="{ 'on-hover': hover }" class="mx-auto" height="250" tile color="#333c51" align="center">
                          <v-card-actions>
                            <v-spacer></v-spacer>
                            <v-btn tile small :color="hover ? '#F34F64' : '#777d8b'" dark>
                              {{ denni.prix }}
                            </v-btn>
                          </v-card-actions>
                          <v-img :src="denni.avatar" width="150" height="150"></v-img>
                          <v-card-text :class="hover ? 'red--text' : 'white--text'">{{ denni.title }}</v-card-text>
                        </v-card>
                      </v-hover>
                    </v-col>
                  </v-row>
                </v-card>
              </v-tab-item>
            </v-tabs-items>
          </v-col>
          <!-- payment -->
          <v-col cols="12" sm="4">
            <Payment />
          </v-col>
        </v-row>
      </v-card>
    </v-container>
  </v-app>
</template>

<script>
import Sidebar from "@/components/Sidebar";
import Navbar from "@/components/Navbar";
import Payment from "@/components/Payment";
export default {
  name: "HomeView",
  components: {
    Sidebar,
    Navbar,
    Payment,
  },
  data() {
    return {
      tab: null,
      parasuts: [
        {
          avatar: require("@/assets/parasut/1.png"),
          prix: "$69",
          title: "Style one Parasut",
        },
        {
          avatar: require("@/assets/parasut/2.png"),
          prix: "$15",
          title: "Style two Parasut",
        },
        {
          avatar: require("@/assets/parasut/3.png"),
          prix: "$28",
          title: "Style three Parasut",
        },
        {
          avatar: require("@/assets/parasut/4.png"),
          prix: "$49",
          title: "Style four Parasut",
        },
        {
          avatar: require("@/assets/parasut/5.png"),
          prix: "$10",
          title: "Style five Parasut",
        },
        {
          avatar: require("@/assets/parasut/6.png"),
          prix: "$39",
          title: "Style six Parasut",
        },
        {
          avatar: require("@/assets/parasut/7.png"),
          prix: "$61",
          title: "Style seven Parasut",
        },
        {
          avatar: require("@/assets/parasut/8.png"),
          prix: "$10",
          title: "Style eight Parasut",
        },
      ],
      parkas: [
        {
          avatar: require("@/assets/parka/1.png"),
          prix: "$69",
          title: "Style one Parasut",
        },
        {
          avatar: require("@/assets/parka/2.png"),
          prix: "$28",
          title: "Style two Parka",
        },
        {
          avatar: require("@/assets/parka/3.png"),
          prix: "$12",
          title: "Style three Parka",
        },
        {
          avatar: require("@/assets/parka/4.png"),
          prix: "$69",
          title: "Style four Parka",
        },
        {
          avatar: require("@/assets/parka/5.png"),
          prix: "$40",
          title: "Style five Parka",
        },
        {
          avatar: require("@/assets/parka/6.png"),
          prix: "$27",
          title: "Style six Parka",
        },
        {
          avatar: require("@/assets/parka/7.png"),
          prix: "$16",
          title: "Style seven Parka",
        },
        {
          avatar: require("@/assets/parka/8.png"),
          prix: "$71",
          title: "Style eight Parka",
        },
      ],
      steves: [
        {
          avatar: require("@/assets/steve/1.png"),
          prix: "$69",
          title: "Style one Steve",
        },
        {
          avatar: require("@/assets/steve/2.png"),
          prix: "$19",
          title: "Style two Steve",
        },
        {
          avatar: require("@/assets/steve/3.png"),
          prix: "$49",
          title: "Style three Steve",
        },
        {
          avatar: require("@/assets/steve/4.png"),
          prix: "$75",
          title: "Style four Steve",
        },
        {
          avatar: require("@/assets/steve/5.png"),
          prix: "$28",
          title: "Style five Steve",
        },
        {
          avatar: require("@/assets/steve/6.png"),
          prix: "$36",
          title: "Style six Steve",
        },
        {
          avatar: require("@/assets/steve/7.png"),
          prix: "$47",
          title: "Style seven Steve",
        },
        {
          avatar: require("@/assets/steve/8.png"),
          prix: "$19",
          title: "Style eight Steve",
        },
      ],
      dennis: [
        {
          avatar: require("@/assets/dennis/1.png"),
          prix: "$69",
          title: "Style one Dennis",
        },
        {
          avatar: require("@/assets/dennis/2.png"),
          prix: "$86",
          title: "Style two Dennis",
        },
        {
          avatar: require("@/assets/dennis/3.png"),
          prix: "$42",
          title: "Style three Dennis",
        },
        {
          avatar: require("@/assets/dennis/4.png"),
          prix: "$26",
          title: "Style four Dennis",
        },
        {
          avatar: require("@/assets/dennis/5.png"),
          prix: "$80",
          title: "Style five Dennis",
        },
        {
          avatar: require("@/assets/dennis/6.png"),
          prix: "$12",
          title: "Style six Dennis",
        },
        {
          avatar: require("@/assets/dennis/7.png"),
          prix: "$27",
          title: "Style seven Dennis",
        },
        {
          avatar: require("@/assets/dennis/8.png"),
          prix: "$35",
          title: "Style eight Dennis",
        },
      ],
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

.container {
  padding: 0px !important;
}

.v-card.card_global {
  height: 800px !important;
}

.theme--light.v-card.card_item {
  background-color: #323b50 !important;
  color: #babec9;
}

.v-sheet.v-card.card_item {
  border-radius: 0px !important;
}

.v-btn:not(.v-btn--round).v-size--small {
  width: 50px !important;
}

.v-application .red--text {
  color: #f34f64 !important;
  caret-color: #f34f64 !important;
}
</style>
