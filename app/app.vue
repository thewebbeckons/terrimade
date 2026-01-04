<script setup>
useHead({
  meta: [
    { name: 'viewport', content: 'width=device-width, initial-scale=1' }
  ],
  link: [
    { rel: 'icon', href: '/favicon.ico' },
    { rel: 'preconnect', href: 'https://fonts.googleapis.com' },
    { rel: 'preconnect', href: 'https://fonts.gstatic.com', crossorigin: '' },
    { rel: 'stylesheet', href: 'https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;500;600;700&display=swap' }
  ],
  htmlAttrs: {
    lang: 'en'
  }
})

const title = 'Beckcraft'
const description = 'Beckcraft is an artisanal quilting studio based in Toronto, Canada'

useSeoMeta({
  title,
  description,
  ogTitle: title,
  ogDescription: description,
  ogImage: '/og-image.png',
  twitterImage: '/og-image.png',
  twitterCard: 'summary_large_image'
})

const cartOpen = ref(false)
</script>

<template>
  <UApp class="bg-canvas min-h-screen">
    <div class="absolute top-0 left-0 right-0 z-50 pointer-events-none">
      <AppHeader v-model:cart-open="cartOpen" />
    </div>

    <main>
      <NuxtPage />
    </main>

    <AppFooter />

    <CartSlideover v-model:open="cartOpen" />
  </UApp>
</template>

