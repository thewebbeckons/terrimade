<script setup lang="ts">
import type { NavigationMenuItem } from '@nuxt/ui'

const cartOpen = defineModel<boolean>('cartOpen', { default: false })
const cartCount = ref(0)

const navItems: NavigationMenuItem[] = [
  { label: 'About', to: '/about' },
  { label: 'Shop', to: '/shop' },
  { label: 'Community', to: '/community' }
]
</script>

<template>
  <header class="fixed top-0 left-0 right-0 z-50 p-4 md:p-6">
    <div class="mx-auto max-w-7xl bg-warm-50/90 backdrop-blur-md shadow-warm rounded-sm px-6 md:px-10 py-3 flex items-center justify-between">
      <!-- Left: Navigation Menu -->
      <nav class="flex-1">
        <UNavigationMenu
          :items="navItems"
          variant="link"
          :ui="{
            link: 'text-sm font-sans uppercase tracking-wider text-ink-soft hover:text-sage-600 transition-colors duration-300'
          }"
        />
      </nav>

      <!-- Center: Logo -->
      <NuxtLink 
        to="/" 
        class="font-serif text-2xl md:text-3xl text-ink tracking-tight hover:text-sage-600 transition-colors duration-300"
      >
        <span class="italic font-light mr-1">beck</span><span class="font-semibold">craft</span>
      </NuxtLink>

      <!-- Right: Cart Button -->
      <div class="flex-1 flex justify-end">
        <button
          class="text-xs font-sans uppercase tracking-widest text-ink-soft hover:text-sage-600 transition-colors duration-300"
          @click="cartOpen = true"
        >
          Bag ({{ cartCount }})
        </button>
      </div>
    </div>
  </header>
</template>

