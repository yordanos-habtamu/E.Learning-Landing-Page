<template>
  <v-sheet
    elevation="2"
    rounded="lg"
    class="d-flex flex-column align-center justify-center"
    color="primary"
    style="height: auto; width: 100%; margin-top: 25px;"
  >
    <h1 class="text-center pt-5 text-white font-weight-bold text-h3">
      Testimonies From Our Students
    </h1>
    <p class="text-white text-center mb-8">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit, ab!
    </p>

    <v-container>
      <v-row>
        <v-col
          v-for="(info, i) in infos"
          :key="i"
          cols="12"
          sm="6"
          md="4"
          lg="3"
          class="d-flex"
        >
          <v-card class="mx-auto mt-6 h-100 d-flex flex-column" max-width="300">
            <v-card-title class="d-flex align-center">
              <v-avatar size="40" variant="outlined" class="mr-3">
                <v-img :src="info.img" />
              </v-avatar>
              <div>
                <div class="font-weight-bold">{{ info.fullname }}</div>
                <div class="text-caption text-grey-darken-1">{{ info.sub }}</div>
              </div>
            </v-card-title>

            <v-card-text>
              "{{ info.testimony }}"
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-sheet>
</template>

<script setup lang="ts">
import { reactive } from "vue";

const infos = reactive([
  {
    img: "/stu.jpg",
    title: "Complete Web Design",
    sub: "Artificial Intelligence",
    fullname: "John Doe",
    testimony:
      "This platform helped me land my first tech job. The instructors were amazing!",
  },
  {
    img: "/stu.jpg",
    title: "Data Science Bootcamp",
    sub: "Machine Learning",
    fullname: "Jane Smith",
    testimony:
      "The best learning experience I've had. The projects were very practical.",
  },
  {
    img: "/stu.jpg",
    title: "Mobile App Development",
    sub: "Flutter & Dart",
    fullname: "Michael Lee",
    testimony:
      "I loved the hands-on approach. Highly recommend for aspiring developers!",
  },
    {
    img: "/stu.jpg",
    title: "Mobile App Development",
    sub: "Flutter & Dart",
    fullname: "Michael Lee",
    testimony:
      "I loved the hands-on approach. Highly recommend for aspiring developers!",
  },
]);
</script>
