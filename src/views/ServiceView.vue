<template>
  <div>
   <!-- Header -->
    <Header>
      <template #head-title>{{ headerData.title }}</template>
      <template #content-body>{{ headerData.description }}</template>
    </Header>

    <!-- Services Section -->
    <section class="py-12 px-6 max-w-6xl mx-auto">
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <!-- Service Card 1 -->
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
    { title: 'UI/UX Design', content: 'Designs that are both beautiful and user-friendly.' },
    { title: 'SEO Optimization', content: 'We help your website rank higher in search engines.' },
    { title: 'E-commerce Solutions', content: 'We create online stores that sell products and services.' },
    { title: 'Digital Marketing', content: 'Strategies to boost your online presence and engagement.' }
]);
const headerData = reactive({
  title: 'Our Services',
  description: 'We offer a wide range of digital solutions to help you grow.'
});
import Header from '../components/Header.vue';
import Card from '../components/Card.vue';
</script>