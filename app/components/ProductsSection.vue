<template>
  <section class="py-20 md:py-32 bg-canvas">
    <div class="container mx-auto px-4 md:px-6 lg:px-8">
      <!-- Header -->
      <div class="text-center mb-16">
        <span class="text-xs font-mono uppercase tracking-widest text-sage-500 mb-3 block">
          {{ eyebrow }}
        </span>
        <h2 class="font-serif text-4xl md:text-5xl text-ink mb-4">
          {{ title }}
        </h2>
        <p v-if="description" class="text-ink-soft text-lg max-w-xl mx-auto">
          {{ description }}
        </p>
      </div>
      
      <!-- Products Grid -->
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-8 md:gap-10">
        <ProductCard
          v-for="(product, index) in products"
          :key="product.name"
          :product="product"
          :style="{ animationDelay: `${index * 0.1}s` }"
        />
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import type { Product } from './ProductCard.vue'

withDefaults(defineProps<{
  eyebrow?: string
  title: string
  description?: string
  products: Product[]
}>(), {
  eyebrow: 'Handcrafted'
})
</script>
