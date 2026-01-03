<script setup lang="ts">
const collections = [
  { name: 'Cotton', to: '/collections/cotton' },
  { name: 'Linen', to: '/collections/linen' },
  { name: 'Weighted', to: '/collections/weighted' },
  { name: 'Baby', to: '/collections/baby' },
  { name: 'Journal', to: '/journal' }
]
</script>

<template>
  <footer class="bg-warm-300 text-ink">
    <div class="px-6 md:px-10 lg:px-16 py-16">
      <div class="grid grid-cols-1 md:grid-cols-3 gap-12 mb-12 max-w-7xl mx-auto">
        <!-- Shop Column -->
        <div>
          <h3 class="font-serif text-lg mb-6">Shop</h3>
          <ul class="space-y-3">
            <li v-for="item in collections" :key="item.name">
              <NuxtLink
                :to="item.to"
                class="text-sm text-ink-soft hover:text-sage-600 transition-colors"
              >
                {{ item.name }}
              </NuxtLink>
            </li>
          </ul>
        </div>

        <!-- About Column -->
        <div>
          <h3 class="font-serif text-lg mb-6">About</h3>
          <ul class="space-y-3">
            <li>
              <NuxtLink to="/about" class="text-sm text-ink-soft hover:text-sage-600 transition-colors">
                Our Story
              </NuxtLink>
            </li>
            <li>
              <NuxtLink to="/journal" class="text-sm text-ink-soft hover:text-sage-600 transition-colors">
                Journal
              </NuxtLink>
            </li>
            <li>
              <NuxtLink to="/contact" class="text-sm text-ink-soft hover:text-sage-600 transition-colors">
                Contact
              </NuxtLink>
            </li>
          </ul>
        </div>

        <!-- Newsletter Column -->
        <div>
          <h3 class="font-serif text-lg mb-6">Stay Warm</h3>
          <p class="text-sm text-ink-soft mb-4">
            Join our newsletter for new collections and quiet updates.
          </p>
          <form class="space-y-3">
            <UInput
              type="email"
              placeholder="your@email.com"
              class="bg-canvas border-warm-400 text-ink placeholder:text-ink-soft/50 rounded-md"
            />
            <UButton
              color="primary"
              variant="solid"
              class="w-full rounded-full"
            >
              Subscribe
            </UButton>
          </form>
        </div>
      </div>

      <div class="flex flex-col md:flex-row justify-between items-center pt-8 border-t border-warm-400 max-w-7xl mx-auto">
        <p class="text-xs text-ink-soft">
          © {{ new Date().getFullYear() }} Terrimade. Handcrafted in Toronto.
        </p>
        <div class="flex gap-6 mt-4 md:mt-0">
          <NuxtLink to="/privacy" class="text-xs text-ink-soft hover:text-sage-600 transition-colors">
            Privacy
          </NuxtLink>
          <NuxtLink to="/terms" class="text-xs text-ink-soft hover:text-sage-600 transition-colors">
            Terms
          </NuxtLink>
        </div>
      </div>
    </div>
  </footer>
</template>
