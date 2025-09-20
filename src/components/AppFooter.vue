<template>
  <v-footer color="primary" flat class="text-white py-12 px-6 mt-10" width="100%">
    <v-container>
      <v-row>
        <!-- Brand + Social -->
        <v-col cols="12" sm="6" md="4" class="mb-6">
          <h2 class="font-weight-bold mb-4">E.<span>Learning</span></h2>
          <div class="d-flex">
            <v-btn
              v-for="icon in icons"
              :key="icon"
              class="mx-1"
              variant="text"
              icon
            >
              <v-icon size="24">{{ icon }}</v-icon>
            </v-btn>
          </div>
        </v-col>

        <!-- About -->
        <v-col cols="12" sm="6" md="3" class="mb-6">
          <h3 class="font-weight-bold mb-3">About</h3>
          <p class="text-grey-lighten-3">How it Works?</p>
          <p class="text-grey-lighten-3">Our Programs</p>
          <p class="text-grey-lighten-3">Promotions</p>
          <p class="text-grey-lighten-3">Refer a Friend</p>
        </v-col>

        <!-- Delivery -->
        <v-col cols="12" sm="6" md="3" class="mb-6">
          <h3 class="font-weight-bold mb-3">Delivery</h3>
          <p class="text-grey-lighten-3">Cost on Delivery</p>
          <p class="text-grey-lighten-3">Delivery Status</p>
          <p class="text-grey-lighten-3">Delivery Method</p>
          <p class="text-grey-lighten-3">Returns</p>
        </v-col>

        <!-- Contacts -->
        <v-col cols="12" sm="6" md="2" class="mb-6">
          <h3 class="font-weight-bold mb-3">Contacts</h3>
          <p class="text-grey-lighten-3">E.Learning</p>
          <p class="text-grey-lighten-3">Adiss Road</p>
          <p class="text-grey-lighten-3">+251 123 456 789</p>
          <p class="text-grey-lighten-3">support@elearning.com</p>
        </v-col>
      </v-row>
    </v-container>
  </v-footer>
</template>

<script setup lang="ts">
import { reactive } from "vue";

const icons = reactive([
  "mdi-apple",
  "mdi-google-plus",
  "mdi-twitter",
  "mdi-facebook",
]);
</script>
