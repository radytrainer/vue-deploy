<template>
  <div>
 <!-- Header -->
    <Header>
      <template #head-title>{{ headerData.title }}</template>
      <template #content-body>{{ headerData.description }}</template>
    </Header>

    <!-- Contact Form Section -->
    <section class="py-12 px-6 max-w-4xl mx-auto">
      <div class="bg-white shadow-md rounded-xl p-8">
        <form @submit.prevent="submitForm" class="space-y-6">
          <div>
            <label class="block text-gray-700 mb-1 font-medium">Name</label>
            <input
              v-model="form.name"
              type="text"
              class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-400"
              required
            />
          </div>
          <div>
            <label class="block text-gray-700 mb-1 font-medium">Email</label>
            <input
              v-model="form.email"
              type="email"
              class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-400"
              required
            />
          </div>
          <div>
            <label class="block text-gray-700 mb-1 font-medium">Message</label>
            <textarea
              v-model="form.message"
              rows="5"
              class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-400"
              required
            ></textarea>
          </div>
          <button
            type="submit"
            class="bg-blue-600 text-white px-6 py-2 rounded-lg hover:bg-blue-700 transition"
          >
            Send Message
          </button>
        </form>
      </div>

      <!-- Contact Info -->
      <div class="mt-12 text-center text-gray-700">
        <p><strong>Email:</strong> contact@example.com</p>
        <p><strong>Phone:</strong> +855 123 456 789</p>
        <p><strong>Address:</strong> Phnom Penh, Cambodia</p>
      </div>
    </section>
  </div>
</template>

<script setup>
import { reactive } from 'vue'

const form = reactive({
  name: '',
  email: '',
  message: ''
})

const submitForm = () => {
  alert(`Thank you, ${form.name}! We’ll get back to you soon.`)
  form.name = ''
  form.email = ''
  form.message = ''
}
const headerData = reactive({
  title: 'Contact Us',
  description: 'We would love to hear from you! Please fill out the form below.'
})
import Header from '../components/Header.vue';
</script>
