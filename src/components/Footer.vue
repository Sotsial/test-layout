<template>
  <v-footer color="#163454" inset absolute app padless>
    <v-row no-gutters class="my-5">
      <v-col v-if="!$vuetify.breakpoint.xs"></v-col>
      <v-col class="pl-5">
        <div>Контакты</div>
        <div>О компании</div>
        <div>Контакты</div>
        <div>О компании</div>
      </v-col>
      <v-col v-if="!$vuetify.breakpoint.xs">
        <div>Платежи</div>
        <div>Тарифы</div>
        <div>Платежи</div>
        <div>Тарифы</div>
      </v-col>
      <v-col v-if="!$vuetify.breakpoint.xs">
        <div>Контакты</div>
        <div>О компании</div>
        <div>Контакты</div>
        <div>О компании</div>
      </v-col>
      <v-col>
        <div>Платежи</div>
        <div>Тарифы</div>
        <div>Платежи</div>
        <div>Тарифы</div>
      </v-col>

      <v-col v-if="!$vuetify.breakpoint.xs">
        <v-img src="@/assets/visa.png" width="100px" class="mb-2" />
        <v-img src="@/assets/gpay.png" width="50px" class="mb-2" />
        <v-img src="@/assets/apay.png" width="50px" />
      </v-col>
      <v-col class="d-flex align-center">
        <v-btn color="#547DA9" dark>Справка</v-btn>
      </v-col>
    </v-row>
  </v-footer>
</template>

<style scoped lang="scss">
footer {
  font-size: 14px;
}

div {
  color: #d3e4f480;
  :hover {
    color: #ffff;
  }
}
</style>
