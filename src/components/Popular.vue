<template>
   <v-sheet elevation="2" rounded="lg" color="primary" style="height: 600px; width:100%;margin-top:25px; padding:15px;">
    <h1 class="text-center pt-5 text-white font-weight-bold text-h3" >
        Our Popular Courses
    </h1>
    <p class="text-white text-center">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit, ab!
    </p>
    <v-row>
        <v-col cols="4" v-for="(info,i) in infos.infos" :key="i">
           <v-hover v-slot="{ hover }">
  <v-card
    :elevation="hover ? 12 : 2"
    class="mx-4 mt-4"
    max-width="400"
    :style="{
      transform: hover ? 'scale(1.05)' : 'scale(1)',
      transition: 'all 0.3s ease',
    }"
  >
    <template v-slot:loader="{ isActive }">
      <v-progress-linear
        :active="isActive"
        color="deep-purple"
        height="4"
        indeterminate
      />
    </template>

    <v-img height="200" :src="info.img" cover class="ma-2"></v-img>

    <v-card-item class="mt-6">
      <v-toolbar color="transparent">
        <v-btn class="text-none" color="purple-lighten-3" variant="flat">
          <template v-slot:prepend>
            <v-icon color="white" icon="mdi-brightness-1"></v-icon>
          </template>
          {{ info.bt1 }}
        </v-btn>
        <v-spacer></v-spacer>
        <v-btn
          class="text-none"
          color="primary"
          variant="flat"
          prepend-icon="mdi-star"
        >
          {{ info.bt2 }}
        </v-btn>
      </v-toolbar>

      <v-card-title>{{ info.title }}</v-card-title>
      <v-card-subtitle>
        <v-icon color="primary" icon="mdi-open-blank-variant" size="small" />
        <span class="ml-2">{{ info.student }}</span>
      </v-card-subtitle>
    </v-card-item>

    <v-divider class="mx-4 mb-1"></v-divider>

    <v-card-actions>
      <span>{{ info.money }}</span>
      <v-spacer></v-spacer>
      <v-avatar>
        <v-img alt="John" src="http://cdn.vuetifyjs.com/images/john.jpg"></v-img>
      </v-avatar>
      <span>{{ info.fullname }}</span>
    </v-card-actions>
  </v-card>
</v-hover>


        </v-col>
    </v-row>

   </v-sheet>
</template>
<script setup lang="ts">
import {reactive} from 'vue'
const infos = reactive({
    loading:false,
    selection:1,
    infos:[{
        img:"/stu.jpg",
        bt1:"Web Design",
        bt2:"4.9 (234)",
        title:"Complete Web Design",
        student:"1000 Students",
        money:"$10",
        fullname:"John Doe",
        book:"27 classes"
    },
{
        img:"/stu.jpg",
        bt1:"Web Design",
        bt2:"4.9 (234)",
        title:"Complete Web Design",
        student:"1000 Students",
        money:"$10",
        fullname:"John Doe",
        book:"27 classes"
    },
    {
        img:"/stu.jpg",
        bt1:"Web Design",
        bt2:"4.9 (234)",
        title:"Complete Web Design",
        student:"1000 Students",
        money:"$10",
        fullname:"John Doe",
        book:"27 classes"
    },
 
]
})
</script>