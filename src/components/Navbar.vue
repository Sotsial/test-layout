<template>
  <v-app-bar app flat clipped-left class="white">
    <v-container class="d-flex">
      <v-img
        src="@/assets/logo.png"
        :max-width="$vuetify.breakpoint.xs ? 100 : 150"
        contain
      ></v-img>

      <v-spacer />
      <v-btn plain color="#436D9B" class="px-0">
        <v-icon v-if="!$vuetify.breakpoint.xs"
          >mdi-account-circle-outline</v-icon
        >
        <div class="font-weight-bold ml-1">
          Профиль
        </div>
      </v-btn>

      <v-btn plain color="#436D9B">
        <v-icon v-if="!$vuetify.breakpoint.xs">mdi-exit-to-app</v-icon>
        <div class="font-weight-bold ml-1">
          Выход
        </div>
      </v-btn>
    </v-container>
  </v-app-bar>
</template>
