<template>
  <div class="overflow-x-hidden bg-canvas">
    <!-- Hero Section -->
    <section class="relative min-h-screen flex items-center justify-center overflow-hidden">
      <!-- Background Image -->
      <NuxtImg 
        src="/humber_bg.jpeg" 
        alt="Humber River" 
        class="absolute inset-0 w-full h-full object-cover"
      />
      
      <!-- Glassmorphism Overlay with Moving Sage Gradient -->
      <div 
        class="absolute inset-0 z-0 bg-gradient-to-br from-sage-500/60 via-sage-400/50 to-sage-600/60 animate-background-shift backdrop-blur-md"
      />
  
      <!-- Hero Content -->
      <div class="relative z-10 text-center px-4">
        <!-- Flip Words Display -->
        <h1 class="font-serif text-8xl lg:text-9xl text-warm-50 leading-tight mb-6 animate-fade-in flex flex-col md:flex-row md:items-baseline justify-center">
          <FlipWords
            :words="['wood', 'quilt', 'art', 'beck']"
            :duration="2500"
            class="italic font-light"
          /><span class="font-semibold">craft</span>
        </h1>
        
        <!-- Tagline -->
        <p 
          class="text-lg md:text-xl text-warm-100/80 mt-8 max-w-md mx-auto animate-fade-in-up font-sans"
          style="animation-delay: 0.3s;"
        >
          Handcrafted woodwork, quilts & paintings from Toronto
        </p>
      </div>

      <!-- Scroll Indicator -->
      <div class="absolute bottom-8 left-1/2 -translate-x-1/2 animate-bounce">
        <div class="w-6 h-10 border-2 border-warm-100/30 rounded-full flex justify-center">
          <div class="w-1 h-3 bg-warm-100/40 rounded-full mt-2" />
        </div>
      </div>
    </section>
    
    <!-- Featured Collection Section -->
    <ProductsSection
      eyebrow="Handcrafted"
      title="Featured Collection"
      description="Each piece crafted with care, designed for lasting beauty"
      :products="products"
    />

    <!-- Story Section -->
    <section class="py-20 md:py-32 bg-warm-200">
      <div class="container mx-auto px-4 md:px-6 lg:px-8">
        <div class="grid lg:grid-cols-2 gap-12 lg:gap-20 items-center">
          <div>
            <NuxtImg
              src="/quilt.png"
              alt="Craftsmanship detail"
              class="w-full h-auto rounded-lg shadow-warm-lg"
            />
          </div>
          <div>
            <span class="text-xs font-mono uppercase tracking-widest text-sage-500 mb-4 block">
              Our Process
            </span>
            <h2 class="font-serif text-4xl md:text-5xl text-ink leading-tight mb-6">
              Crafted,<br />
              <em class="font-light">With Care</em>
            </h2>
            <p class="text-ink-soft text-lg leading-relaxed mb-6">
              Every piece begins with a conversation — about beauty, about memory, about the spaces we call home. From hand-turned wood to stitched quilts to original paintings, we create with intention.
            </p>
            <p class="text-ink-soft text-lg leading-relaxed mb-8">
              The result is more than a product. It's an heirloom.
            </p>

          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
import type { Product } from '~/components/ProductCard.vue'

const products = ref<Product[]>([
  {
    name: 'Maple Serving Board',
    category: 'woodwork',
    price: 125,
    image: '/maple-board.png'
  },
  {
    name: 'Sunday Morning Quilt',
    category: 'quilts',
    price: 285,
    image: '/sunday-quilt.png'
  },
  {
    name: 'Lakeside Morning',
    category: 'paintings',
    price: 450,
    image: '/lakeside-painting.png'
  },
  {
    name: 'Walnut Bowl Set',
    category: 'woodwork',
    price: 175,
    image: '/walnut-bowls.png'
  }
])
</script>

<style scoped>
/* Animation styles moved to ProductCard component */
</style>
