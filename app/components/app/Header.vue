<script setup lang="ts">
import type { NavigationMenuItem } from '@nuxt/ui'

const cartOpen = defineModel<boolean>('cartOpen', { default: false })
const cartCount = ref(0)
const isMobileOpen = ref(false)

const navItems: NavigationMenuItem[] = [
  { label: 'About', to: '/about' },
  { label: 'Shop', to: '/shop' },
  { label: 'Community', to: '/community' }
]
</script>

<template>
  <UHeader
    v-model:open="isMobileOpen"
    toggle-side="left"
    mode="slideover"
    :ui="{
      root: 'fixed top-0 left-0 right-0 z-50 p-4 md:p-6 transition-all duration-300 pointer-events-none bg-transparent backdrop-blur-none border-none',
      container: 'mx-auto max-w-7xl bg-warm-50/90 backdrop-blur-md shadow-warm rounded-sm px-4 md:px-10 py-3 flex items-center justify-between pointer-events-auto min-h-[4rem]',
      left: 'flex-1 flex items-center gap-4',
      center: 'flex-0',
      right: 'flex-1 flex items-center justify-end gap-4',
      toggle: 'md:hidden text-ink-soft hover:text-sage-600 transition-colors order-first mr-4'
    }"
  >
    <!-- Left: Navigation (Desktop) & Logo (Mobile) -->
    <template #left>
      <!-- Mobile Logo (visible only on mobile, next to toggle) -->
      <NuxtLink 
        to="/" 
        class="md:hidden font-serif text-2xl text-ink tracking-tight hover:text-sage-600 transition-colors duration-300"
      >
        <span class="italic font-light mr-1">beck</span><span class="font-semibold">craft</span>
      </NuxtLink>

      <!-- Desktop Navigation -->
      <nav class="hidden md:block">
        <UNavigationMenu
          :items="navItems"
          variant="link"
          :ui="{
            link: 'text-sm font-sans uppercase tracking-wider text-ink-soft hover:text-sage-600 transition-colors duration-300'
          }"
        />
      </nav>
    </template>

    <!-- Center: Logo (Desktop Only) -->
    <template #default>
      <NuxtLink 
        to="/" 
        class="hidden md:block font-serif text-3xl text-ink tracking-tight hover:text-sage-600 transition-colors duration-300"
      >
        <span class="italic font-light mr-1">beck</span><span class="font-semibold">craft</span>
      </NuxtLink>
    </template>

    <!-- Right: Cart Button -->
    <template #right>
      <button
        class="text-xs font-sans uppercase tracking-widest text-ink-soft hover:text-sage-600 transition-colors duration-300"
        @click="cartOpen = true"
      >
        Bag ({{ cartCount }})
      </button>
    </template>

    <!-- Mobile Slideover Body -->
    <template #body>
      <div class="p-6 space-y-4">
        <UNavigationMenu
          :items="navItems"
          orientation="vertical"
          variant="link"
          :ui="{
            link: 'text-lg font-serif py-3 text-ink hover:text-sage-600 transition-colors'
          }"
          @click="isMobileOpen = false"
        />
      </div>
    </template>
  </UHeader>
</template>

