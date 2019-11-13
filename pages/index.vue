<template>
  <div class="container mx-auto px-4">
    <div class="text-center mt-16">
      <logo />
      <h1 class="mt-8 mb-4 text-4xl font-semibold text-blue-800">
        Tailwind CSS Playground
      </h1>
      <h2 class="text-xl font-semibold">
        Few sample of Tailwind components
      </h2>
      <section class="flex justify-center my-16">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          class="btn hover:border-teal-600"
        >
          Nuxt documentation
        </a>
        <a
          href="https://tailwindcss.com/"
          target="_blank"
          class="btn hover:border-teal-600 ml-3"
        >
          Tailwind documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="btn hover:border-teal-600 ml-3"
        >
          GitHub
        </a>
      </section>

      <section>
        <nuxt-link
          v-for="item in menu"
          :key="item.routeName"
          :to="{ name: item.routeName }"
          class="mr-3 last:mr-0 btn border-blue-400 hover:border-blue-600 text-blue-400 hover:text-blue-600"
        >
          {{ item.title }}
        </nuxt-link>
      </section>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  },

  data() {
    return {
      menu: [
        { title: 'Responsive menu', routeName: 'menu' },
        {
          title: 'Stripe-style animated vertical tabs',
          routeName: 'stripe-style-animated-vertical-tabs'
        }
      ]
    }
  }
}
</script>

<style>
.btn {
  @apply px-3 py-2 border rounded;
}
</style>
