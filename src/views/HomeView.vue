<template>
  <v-col cols="12" md="8" class="mx-auto">
    <v-row no-gutters>
      <v-col
        v-for="(item, i) in 4"
        :key="i"
        cols="12"
        sm="6"
        md="6"
        lg="5"
        xl="3"
      >
        <v-card
          class="mx-auto my-12"
          width="280"
        >
          <v-img
            cover
            height="250"
            src="@/assets/item_preview.svg"
          />
          <v-card-item>
            <v-card-title>Cashmere II</v-card-title>

            <v-card-subtitle>
              <span class="me-1">Покрывало</span>
            </v-card-subtitle>
          </v-card-item>
          <v-card-actions>
            <v-row
              justify="space-between"
              align="center"
              class="mx-0"
            >
              <v-col>
                <p>219 000 ₽</p>
              </v-col>
              <v-img 
                contain
                max-width="16.55"
                max-height="20"
                src="@/assets/buy.svg"
              />
            </v-row>  
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
    <v-row no-gutters class="mt-5 mb-1">
      <v-spacer />
      <v-btn class="showMoreBtn" width="142" height="25">Показать еще</v-btn>
    </v-row>
    <v-footer height="150"></v-footer>
  </v-col>
</template>

<script>
import axios from 'axios'
export default {
  name: 'HomeView',
  mounted() {
    axios.get('https://api.platovcorp.site/product.json')
      .then(function (response) {
        // handle success
        console.log(response);
      })
      .catch(function (error) {
        // handle error
        console.log(error);
      })
  }
}
</script>

<style scoped>
  .showMoreBtn {
    text-transform: unset;
  }
</style>
