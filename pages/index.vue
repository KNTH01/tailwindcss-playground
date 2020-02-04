<template>
  <div class="container px-4 mx-auto">
    <div class="mt-16 text-center">
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
          class="ml-3 btn hover:border-teal-600"
        >
          Tailwind documentation
        </a>
        <a
          href="https://github.com/KevinNTH/tailwindcss-playground"
          target="_blank"
          class="ml-3 btn hover:border-teal-600"
        >
          GitHub
        </a>
      </section>

      <section>
        <nuxt-link
          v-for="item in menu"
          :key="item.routeName"
          :to="{ name: item.routeName }"
          class="mr-3 text-blue-400 border-blue-400 last:mr-0 btn hover:border-blue-600 hover:text-blue-600"
        >
          {{ item.title }}
        </nuxt-link>
      </section>

      <footer class="mt-32 mb-8">
        <h3 class="mb-1 text-xl font-semibold text-gray-600">Credits</h3>
        <a href="https://www.tailwindui.com" target="_blank">
          <img
            class="inline-block h-8"
            src="https://refactoring-ui.nyc3.cdn.digitaloceanspaces.com/tailwindui-logo.svg"
            alt="Tailwind UI"
          />
        </a>
      </footer>
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
        },
        {
          title: 'Kanban',
          routeName: 'kanban'
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
