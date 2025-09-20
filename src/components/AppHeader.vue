correct this, <template>
    <div style="height:520px; width:100%;">
        <v-app-bar color="#f4f4fb"  style="padding:16px" flat >
        <v-app-bar-title  style="font-weight:200;font-size:30px; line-height:1.4; ">
         <span style="color:#B672FF">E.Learning</span>
        </v-app-bar-title>
        <v-spacer></v-spacer>
    <v-menu transition="slide-x-transition">
     <template v-slot:activator="{props}">
       <v-btn v-bind="props" append-icon="mdi-chevron-down" class="text-none">
     Courses   
    </v-btn>
     </template>
     <v-list>
        <v-list-item>
            <v-list-item-title>
                Course One
            </v-list-item-title>
            <v-list-item-title>
                Course Two
            </v-list-item-title>
        </v-list-item>
     </v-list>
    </v-menu>
      <v-menu transition="slide-x-transition">
     <template v-slot:activator="{props}">
       <v-btn v-bind="props" append-icon="mdi-chevron-down" class="text-none">
      Teachers   
    </v-btn>
     </template>
     <v-list>
        <v-list-item>
            <v-list-item-title>
                Teacher One
            </v-list-item-title>
            <v-list-item-title>
                Teacher Two
            </v-list-item-title>
        </v-list-item>
     </v-list>
    </v-menu>
      <v-menu transition="slide-x-transition" >
     <template v-slot:activator="{props}">
       <v-btn v-bind="props"  class="text-none" append-icon="mdi-chevron-down">
     Offers   
    </v-btn>
     </template>
     <v-list>
        <v-list-item>
            <v-list-item-title>
                Offer one
            </v-list-item-title>
            <v-list-item-title>
                Offer two
            </v-list-item-title>
        </v-list-item>
     </v-list>
    </v-menu>
    <v-btn style="text-transform:none">Contact</v-btn>
        <v-btn style="text-transform:none" variant="outlined" color="#CD7BDF" class="ml-2" >Sign In</v-btn>
           <v-btn style="text-transform:none" variant="flat" color="#CD7BDF" class="ml-2">Log In</v-btn>
        </v-app-bar>
        <v-row >
            <v-col cols="5" class="CG">
                <h1 class="CT" style="font-weight:700; font-size:45px">
                    Develop your
                </h1 >
                       <h1 class="CT" style="font-weight:700; font-size:45px">
                    Skills in a new
                </h1>
                       <h1 class="CT" style="font-weight:700; font-size:45px">
                    and  Unique way
                </h1>
             <p class="text-gray CT mb-10">
                Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                Illo sunt omnis iste pariatur sapiente voluptas.
             </p>
             <v-btn class="text-none CT" color="#CD7BDF" variant="flat">
                Enroll Now
             </v-btn>
            <v-icon color="primary" icon="mdi-play-circle" class="ml-4"></v-icon>
            <span class="text-caption text-medium-emphasis font-weight-light">
               What's E.Learning? 
            </span>
            </v-col>
            <v-col cols="7" class="justify-center">
                <div class="d-flex justify-center">
                <div class="c1 mt-16">
                    <div class="c2">
                        <v-img class=" rounded-circle" src="/stu.jpg" height="230" width="230" cover>

                        </v-img>
                    </div>
                    <v-card style="margin-left:-600px;" max-width="344" subtitle="Online Course" title="50 +" color="#f5e9f8" class="opacity-70" >
                     <template v-slot:prepend>
                        <v-icon color="#CD7BDF" size="36" class="mt-4" icon="mdi-share-circle" >
                        </v-icon>
                     </template>
                    </v-card>
                         <v-card style="margin-left:-180px; margin-top:300px; margin-right:50px" max-width="344" subtitle="Today of 1000 students" title="UI Design Classes" color="#f5e9f8" class="opacity-70" >
                     <template v-slot:prepend>
                       <v-avatar size="24">
                     <v-img  alt="avatars" src="https://avatars2.githubusercontent.com/u/9064066?v=4&s=460"></v-img>
                       </v-avatar>
                     </template>
                     <template v-slot:actions>
                      <v-btn color="primary" variant="flat" class="text-none ml-15"> Join Now</v-btn>
                     </template>
                    </v-card>
                     <v-card style="margin-right:-600px;" max-width=" 344" subtitle="10k" title="Online Students" color="#f5e9f8" class="opacity-70" >
                      <v-avatar size="24">
                                      <v-img  alt="avatars" src="https://avatars2.githubusercontent.com/u/9064066?v=4&s=460"></v-img>
                       </v-avatar>
                    </v-card>

                </div>
                </div>
     

            </v-col>
        </v-row>
    </div>
    <div style="height:80px; width:100%; background-color:#B672FF ;" class="d-flex align-center justify-space-around mt-10 rounded-lg">
        <v-btn prepend-icon="mdi-microsoft" variant="text" color="white" class="font-weight-bold">Microsoft</v-btn>
        <v-btn prepend-icon="mdi-docker" variant="text" color="white" class="font-weight-bold">Docker</v-btn>
         <v-btn prepend-icon="mdi-vuejs" variant="text" color="white" class="font-weight-bold">Vue</v-btn>
         <v-btn prepend-icon="mdi-aws" variant="text" color="white" class="font-weight-bold">AWS</v-btn>
         <v-btn prepend-icon="mdi-kubernetes" variant="text" color="white" class="font-weight-bold">Kubernetes</v-btn>
         <v-btn prepend-icon="mdi-apple" variant="text" color="white" class="font-weight-bold">Apple</v-btn>                                     <v-btn prepend-icon="mdi-microsoft" variant="text" color="white">Microsoft</v-btn>
    </div>
</template>
<script setup lang="ts">
</script>
<style scoped>
.CG{
    margin-top:100px;
}
.CT{
    margin-left:150px;
}
.topme{
    margin-top:50px;
}
.c1{
  width:250px;
  height:250px;
  border-radius:50%;
  display:flex;
  justify-content: center;
  align-items:center;
  position:relative;
  font-size:24;     
  color:white;
  border:3px dashed #CD7BDF;
  box-sizing:border-box;
}
.c2{
    width:230px;
  height:230px;
  border-radius:50%;
  background-color:#CD7BDF;
  display:flex;
  justify-content: center;
  align-items:center;
  position:absolute;
  font-size:16px;     
  color:white;
  border:3px dashed #CD7BDF;
  font-weight: bold;
}
</style>