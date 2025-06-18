<template>
  <div>
    <!-- Header Section -->
     <!-- Header -->
    <Header>
      <template #head-title>{{ headerData.title }}</template>
      <template #content-body>{{ headerData.description }}</template>
    </Header>

    <!-- Body Section -->
    <section class="py-16 px-6 bg-gray-100 text-center">
      <h2 class="text-2xl font-semibold mb-6">What We Do</h2>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6 max-w-5xl mx-auto">
        <Card v-for="(item, index) in dataInfo" :key="index">
          <template #title>
            <h3 class="text-xl font-bold mb-2">{{ item.title }}</h3>
          </template>
          <template #content>
            <p class="text-gray-700">{{ item.content }}</p>
          </template>
        </Card>
      </div>
    </section>
  </div>
</template>
<script setup>
import { reactive } from 'vue';
const dataInfo = reactive([
  { title: 'Web Development', content: 'We build fast, responsive, and beautiful websites.' },
  { title: 'Mobile Apps', content: 'Cross-platform apps that users love.' },
  { title: 'UI/UX Design', content: 'Designs that are both beautiful and user-friendly.' }
]);
const headerData = reactive({
  title: 'Welcome to Our Company',
  description: 'We are dedicated to delivering high-quality digital solutions.'
});
import Header from '../components/Header.vue';
import Card from '../components/Card.vue';
</script>