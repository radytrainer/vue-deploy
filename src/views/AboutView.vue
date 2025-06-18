<template>
  <div>
    <!-- Header -->
    <Header>
      <template #head-title>{{ headerData.title }}</template>
      <template #content-body>{{ headerData.description }}</template>
    </Header>

    <!-- Body -->
    <section class="px-6 py-12 max-w-4xl mx-auto text-gray-800">
      <h2 class="text-2xl font-semibold mb-4">Who We Are</h2>
      <p class="mb-6">
        We are a passionate team of developers, designers, and problem solvers. Our goal is to create meaningful and effective digital experiences for our clients and communities.
      </p>

      <h2 class="text-2xl font-semibold mb-4">Our Mission</h2>
      <p class="mb-6">
        To deliver high-quality digital solutions that help businesses grow, connect people, and simplify lives using the power of technology.
      </p>

      <h2 class="text-2xl font-semibold mb-4">Our Values</h2>
      <ul class="list-disc list-inside space-y-2">
        <li><strong>Innovation:</strong> We embrace change and constantly improve.</li>
        <li><strong>Integrity:</strong> We are honest, transparent, and respectful.</li>
        <li><strong>Collaboration:</strong> We work together and support each other.</li>
        <li><strong>Excellence:</strong> We strive for the highest quality in everything we do.</li>
      </ul>
    </section>
  </div>
</template>
<script setup>
  import { reactive } from 'vue';
  const headerData = reactive({
    title: 'About Us',
    description: 'Learn more about our mission, values, and team.'
  });
  import Header from '../components/Header.vue';
</script>