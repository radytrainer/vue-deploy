<template>
  <div>
    <nav class="bg-blue-600 text-white px-6 py-4 shadow-md">
      <div class="container mx-auto flex justify-between items-center">
        <div class="text-xl font-bold">Kolodoni</div>
        <div class="space-x-4">
          <router-link to="/" class="hover:underline">Home</router-link>
          <router-link to="/about" class="hover:underline">About</router-link>
          <router-link to="/service" class="hover:underline">Services</router-link>
          <router-link to="/contact" class="hover:underline">Contact</router-link>
        </div>
      </div>
    </nav>

    <main class="p-6">
      <router-view />
    </main>
  </div>
</template>

<style scoped>
.router-link-exact-active {
  font-weight: bold;
}
</style>
