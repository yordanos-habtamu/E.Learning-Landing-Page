<template>
  <div class="mt-16">
    <v-row>
      <!-- LEFT SIDE -->
      <v-col cols="6">
        <h1 class="ml-16 font-weight-bold text-h4">
          If you are certified teacher
        </h1>
        <h1 class="ml-16 font-weight-semibold">
          Then become <span class="text-primary">Instructor</span>
        </h1>
        <p class="text-grey-darken-1 ml-16">
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Nam minima
          totam, omnis at esse magni!
        </p>
        <h1 class="ml-16 mb-10 font-weight-bold text-h4">
          Enjoy many perks
        </h1>

        <!-- TWO LISTS -->
        <v-row class="ml-8 mt-n8 mb-2">
          <v-col cols="6">
            <v-list color="white"> 
              <v-list-item
                v-for="file in files"
                :key="file.title"
                :title="file.title"
              >
                <template #prepend>
                  <v-icon color="primary">mdi-circle</v-icon>
                </template>
              </v-list-item>
            </v-list>
          </v-col>

          <v-col cols="6">
            <v-list>
              <v-list-item
                v-for="folder in folders"
                :key="folder.title"
                :title="folder.title"
              >
                <template #prepend>
                  <v-icon color="primary">mdi-circle</v-icon>
                </template>
              </v-list-item>
            </v-list>
          </v-col>
        </v-row>

        <v-btn class="text-none ml-16" color="#cd7bdf" variant="flat">
          Become an Instructor
        </v-btn>
      </v-col>

      <!-- RIGHT SIDE -->
      <v-col cols="6">
        <div class="d-flex justify-center">
          <div class="cc1 mt-16">
            <div class="cc2">
              <v-img src="/stu.jpg" fit class="ma-2"></v-img>
            </div>
          </div>
        </div>
      </v-col>
    </v-row>
  </div>
</template>

<script setup lang="ts">
import { reactive } from "vue";

const files = reactive([
  { title: "Online Order" },
  { title: "24/7 Service" },
  { title: "Clean Kitchen" },
  { title: "Fast Delivery" },
  { title: "Special Discounts" },
]);

const folders = reactive([
  { title: "Pre-Reservation" },
  { title: "Organized Foodies Place" },
  { title: "Sugar Chefs" },
  { title: "Clean Kitchen" },
]);
</script>

<style scoped>
.v-list {
  background-color: white;
}

.cc1 {
  width: 250px;
  height: 300px;
  border-bottom-left-radius: 50%;
  border-bottom-right-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  font-size: 24px;
  color: white;
  border: 3px dashed #cb7bdf;
  box-sizing: border-box;
}

.cc2 {
  width: 230px;
  height: 270px;
  background-color: #cb7bdf;
  border-bottom-left-radius: 50%;
  border-bottom-right-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  position: absolute;
  font-size: 16px;
  color: white;
  font-weight: bold;
}
</style>
