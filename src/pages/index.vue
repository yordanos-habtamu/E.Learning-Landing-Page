<template>
<v-container>
    <AppHeader/>
    <Courses/>
    <Popular/>
    <Certified/>
    <Student/>
    <AppFooter/>
</v-container>
</template>
<script setup lang="ts">
import AppFooter from '../components/AppFooter.vue';
import AppHeader from '../components/AppHeader.vue';
import Certified from '../components/Certified.vue';
import Courses from '../components/Courses.vue';
import Popular from '../components/Popular.vue';
import Student from '../components/Student.vue';

</script>