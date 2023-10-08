<template>
  <v-col cols="12" md="8" class="mx-auto">
    <v-col
      v-for="(item, i) in 4"
      :key="i"
      cols="12"
    >
      <v-card
        elevation="0"
        width="500"
        max-height="200"
        class="ma-0 pa-0"
      >
        <div class="ma-0 pa-0 d-flex flex-no-wrap justify-space-between">
          <v-img
            src="@/assets/item_preview.svg"
          />
          <div class="flex-grow-1 pa-3">
            <v-row>
              <v-spacer></v-spacer>
              <v-btn icon elevation="0">
                <v-icon>mdi-close</v-icon>
              </v-btn>
            </v-row>
            <v-card-title  class="pa-0 text-h5">
              Cashmere II
            </v-card-title>
            <v-card-subtitle class="pa-0">Покрывало</v-card-subtitle>
            <v-card-actions class="ma-0 pa-0">
              <p class="ma-0 pa-0">219 000 ₽</p>
            </v-card-actions>
          </div>
        </div>
      </v-card>
    </v-col>
  </v-col>
</template>

<script>
export default {
  name: 'CartView'
}
</script>
