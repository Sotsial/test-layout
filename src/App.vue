<template>
  <v-app>
    <navbar />
    <v-navigation-drawer v-model="drawer" color="#547DA9" dark app clipped>
      <v-list nav dense class="d-flex">
        <div>
          <v-icon @click="drawer = !drawer" class="ma-2">mdi-arrow-left</v-icon>
        </div>
        <v-list-item-group>
          <v-list-item v-for="item in sidebarItems" :key="item.id" class="my-0">
            <v-list-item-title>{{ item }}</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

    <v-main class=" lighten-blue-2 mb-2">
      <div class=" lighten-blue-1 d-flex align-center">
        <v-container>
          <v-row class="d-flex align-center">
            <v-col cols="12" sm="6" md="8" class="d-flex align-center py-0">
              <v-app-bar-nav-icon
                v-if="!drawer"
                @click="drawer = !drawer"
                class="ml-1"
              />
              <div class="darken-blue-2 font-weight-bold  pa-4">
                Тестируйте платные подключаемые модули бесплатно 14 дней или
                получайте их бесплатно
              </div>
            </v-col>
            <v-col class="d-flex justify-center">
              <v-btn color="#547da9" class=" px-8 font-weight-bold " dark>
                Подробнее</v-btn
              >
            </v-col>
          </v-row>
        </v-container>
      </div>

      <v-container>
        <v-row>
          <v-col v-for="n in 12" :key="n" cols="12" sm="4" lg="3" xl="2">
            <div class="ma-4 card">
              <div class="d-flex align-end mb-3">
                <v-avatar color="white" rounded size="50" tile></v-avatar>
                <div class="px-2 py-1 ml-3 rounded-lg lighten-blue-1">
                  Бесплатно 14 дней
                </div>
              </div>
              <div class="darken-blue-1 mb-3">
                Интеграция с Amo
                <span class="card__text">
                  - Попробуйте Альбато и убедитесь в этом сами. Простой и
                  удобный интерфейс на русском языке. Бесплатный пробный период
                  14 дней. Отзывчивая тех.поддержка. Бесплатный тест.
                </span>
              </div>
              <v-btn
                small
                color="#547da9"
                class=" rounded-lg font-weight-bold "
                dark
                >Установить</v-btn
              >
            </div>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
    <my-footer />
  </v-app>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import Footer from "@/components/Footer.vue";
export default {
  components: {
    navbar: Navbar,
    "my-footer": Footer,
  },

  data: () => ({
    drawer: null,
    sidebarItems: [
      "Номенклатура товаров",
      "Поставщики товаров",
      "Поступление товаров",
      "Списание товаров",
      "Оприходование товаров",
      "Комплектация товаров",
      "Ревизия товаров",
      "Сменные отчеты",
      "Печать этикеток",
      "Настройки кассира",
      "Отчеты организации",
      "Подключаемые модули",
    ],
  }),
};
</script>

<style scoped lang="scss">
.card {
  font-size: 12px;
  font-weight: 700;
  .card__text {
    font-weight: 500;
  }
}
.lighten-blue-1 {
  background-color: #d3e4f4;
}
.lighten-blue-2 {
  background-color: #eef4fa;
}
</style>
