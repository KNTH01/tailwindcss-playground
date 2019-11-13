<template>
  <div class="text-center mt-16">
    <div class="">
      <logo />
      <h1 class="mt-8 mb-4 text-4xl font-semibold text-blue-800">
        Tailwind CSS Playground
      </h1>
      <h2 class="text-xl font-semibold">
        Few sample of Tailwind components
      </h2>
      <div class="flex justify-center my-16">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          class="px-3 py-2 border rounded hover:border-teal-600"
        >
          Nuxt documentation
        </a>
        <a
          href="https://tailwindcss.com/"
          target="_blank"
          class="px-3 py-2 border rounded hover:border-teal-600 ml-3"
        >
          Tailwind documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="px-3 py-2 border rounded hover:border-teal-600 ml-3"
        >
          GitHub
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  }
}
</script>

<style></style>
