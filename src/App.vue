<template>
  <v-app>
    <v-row justify="center" class="header">
      <v-col cols="12" md="8">
        <v-toolbar color="transparent" height="100">
          <v-toolbar-title>
            <v-img src="@/assets/logo.svg" contain width="145" height="40" />
          </v-toolbar-title>
          <v-spacer />
          <p :class="{activeLink: $route.path === '/'}" class="mx-5 link" @click="$router.push({ name: 'home' })">Главная</p>
          <p :class="{activeLink: $route.path === '/cart'}" class="ml-5 link" @click="$router.push({ name: 'cart' })">Корзина</p>
        </v-toolbar>
      </v-col>
    </v-row>
    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style scoped>
.header {
  max-height: 100px;
}
.link {
  cursor: pointer;
}
.activeLink {
  color: #BA967D;
}
</style>