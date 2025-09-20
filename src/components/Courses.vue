<template>
  <div>
    <v-toolbar flat color="transparent">
      <v-toolbar-title class="text-h5 text-center" style="font-weight:600; font-size:37px;">
        Search Courses
      </v-toolbar-title>
    </v-toolbar>

    <v-row>
      <v-col cols="12">
  <v-text-field
  label="Search for over +5000 courses"
  variant="solo"
  clearable
  hide-details
  single-line
  prepend-inner-icon="mdi-magnify"
  density="comfortable"  
  rounded="pill"
  class="mx-auto"
  style="max-width:700px; height:40px;" 
>
          <template v-slot:append>
            <v-menu>
              <template v-slot:activator="{ props }">
                <v-btn v-bind="props" variant="flat" color="primary" class="rounded-pill">Search Courses</v-btn>
              </template>
            </v-menu>
          </template>
        </v-text-field>
      </v-col>
       <v-col cols="6">
      <div class="d-flex justify-center">
        <div class="c3 mt-16">
            <div class="c4">
                <div class="partie c5">
  <v-img src="/stu.jpg" class="w-40 h-40" cover />
</div>
<div class="partie c6">
  <v-img src="/stu.jpg" class="w-40 h-40" cover />
</div>
<div class="partie c7">
  <v-img src="/stu.jpg" class="w-40 h-40" cover />
</div>
<div class="partie c8">
  <v-img src="/stu.jpg" class="w-40 h-40" cover />
</div>

            </div>
        </div>
      </div>
    </v-col>
    <v-col cols="6" style="margin-top:15px ;">
    <h1 style="font-weight:700;font-size:25px;" class="">
        Benifits From Our Online
    </h1>
    <h1 style="font-weight:700;font-size:25px;" class="">
        Learning
    </h1>
    <v-list lines="two">
        <v-list-item v-for="file in files" :key="file.title" :subtitle="file.subTitle" :title="file.title">
           <template v-slot:prepend>
            <v-avatar :color="file.color" size="40">
                <v-icon color="white">{{file.icon}}</v-icon>
            </v-avatar>

           </template>
        </v-list-item>
    </v-list>
    </v-col>
    </v-row>
   
  </div>

</template>

<script setup lang="ts">
import {ref} from 'vue'

const files=ref([{
    color:"purple-lighten-1",
    icon:"mdi-school",
    subTitle:"  Lorem ipsum dolor sit amet consectetur adipisicing elit. Non, facere?",
    title:"Online Degrees"
},
{
    color:"purple-accent-1",
    icon:"mdi-book-open-variant",
    subTitle:"  Lorem ipsum dolor sit amet consectetur adipisicing elit. Non, facere?",
    title:"Short Courses"
},
{
    color:"purple-lighten-1",
    icon:"mdi-account-circle",
    subTitle:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Non, facere?",
    title:"Training from Experts"
},
{
    color:"purple-accent-1",
    icon:"mdi-play",
    subTitle:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Non, facere?",
    title:"More than 10K Video Materials"
}
]
)
</script>
<style scoped>
.v-list{
    background-color:#faf4fb;
}
.c3{
    width:300px;
    height:300px;
    border-radius:20%;
    display:flex;
    justify-content:center;
    align-items:center;
    position:relative;
    font-size:24px;
    color:#faf4fb;
    border:3px dashed #cd7bdf;
    box-sizing:border-box;
}
.c4{
    width:280px;
    height:280px;
    border-radius:20%;
    display:flex;
    justify-content:center;
    align-items:center;
    position:absolute;
    font-weight: bold;
    overflow:hidden;
    font-size:16x;
    color:white;
    border:3px dashed #cd7bdf;
    box-sizing:border-box;
}
.partie{
    width:50%;
    height:50%;
    position:absolute;
}

.c5{
    top:0;
    left:0;
    background-color: #ff8da6;
    border-bottom-right-radius:40%;
}
.c6{
    top:0;
    left:50%;
    background-color: #b672ff;
    border-bottom-left-radius:40%;
}
.c7{
    top:50%;
    left:0;
    background-color: #b672ff;
    border-top-right-radius:40%; 
}
.c8{
    top:50%;
    left:50%;
    background-color: #ff8da6;
    border-top-left-radius:40%;
}


</style>

