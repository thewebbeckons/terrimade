<script setup lang="ts">
const collections = [
  { name: 'Cotton', to: '/collections/cotton' },
  { name: 'Linen', to: '/collections/linen' },
  { name: 'Weighted', to: '/collections/weighted' },
  { name: 'Baby', to: '/collections/baby' },
  { name: 'Journal', to: '/journal' }
]

const cartCount = ref(0)
</script>

<template>
  <header class="fixed top-0 left-0 right-0 z-50 bg-canvas/80 backdrop-blur-sm border-b border-warm-200">
    <div class="flex items-center justify-between px-6 md:px-10 lg:px-16 py-4">
      <!-- Logo -->
      <NuxtLink to="/" class="font-serif text-2xl text-ink tracking-tight hover:text-sage-600 transition-colors">
        Terrimade
      </NuxtLink>

      <!-- Navigation -->
      <nav class="hidden md:flex items-center gap-8">
        <NuxtLink
          v-for="item in collections"
          :key="item.name"
          :to="item.to"
          class="text-xs font-sans uppercase tracking-widest text-ink-soft hover:text-sage-500 transition-colors duration-300"
        >
          {{ item.name }}
        </NuxtLink>
      </nav>

      <!-- Cart -->
      <NuxtLink
        to="/cart"
        class="text-xs font-sans uppercase tracking-widest text-ink-soft hover:text-sage-500 transition-colors duration-300"
      >
        Bag ({{ cartCount }})
      </NuxtLink>
    </div>
  </header>
</template>
