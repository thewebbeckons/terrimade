<template>
  <div class="product-card group cursor-pointer">
    <div class="flex flex-col h-full">
      <!-- Image Container -->
      <div class="aspect-[3/4] overflow-hidden rounded-sm bg-warm-100 mb-5">
        <NuxtImg
          :src="product.image"
          :alt="product.name"
          class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-105"
        />
      </div>
      
      <!-- Content -->
      <div class="flex flex-col flex-1">
        <!-- Title -->
        <h3 class="font-serif text-xl md:text-2xl text-ink leading-snug mb-4">
          {{ product.name }}
        </h3>
        
        <!-- Bottom Row: Category Tag + Price -->
        <div class="flex items-center justify-between mt-auto pt-2">
          <span 
            class="inline-block px-3 py-1.5 text-xs font-mono uppercase tracking-wide text-ink-soft bg-warm-200 rounded-full"
          >
            {{ product.category }}
          </span>
          <span class="font-mono text-sm text-ink-soft">
            ${{ product.price.toFixed(2) }}
          </span>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
export interface Product {
  name: string
  category: string
  price: number
  image: string
}

defineProps<{
  product: Product
}>()
</script>

<style scoped>
.product-card {
  opacity: 0;
  animation: fadeInUp 0.6s ease-out forwards;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(24px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
