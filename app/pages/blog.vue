<template>
  <div class="overflow-x-hidden">
    <!-- Hero Section -->
    <div
      ref="heroRef"
      class="hero-section relative bg-cover bg-center bg-no-repeat min-h-[500px] md:min-h-[600px] flex items-center overflow-hidden"
      :style="{
        backgroundImage: 'url(/hero.png)'
      }"
    >
      <!-- Gradient Overlay -->
      <div class="absolute inset-0 bg-gradient-to-br from-white/60 via-white/40 to-transparent" />
      <div class="absolute inset-0 bg-gradient-to-t from-white/80 via-transparent to-transparent" />
      
      <!-- Animated Background Pattern -->
      <div class="absolute inset-0 opacity-5">
        <div class="absolute inset-0 bg-[radial-gradient(circle_at_50%_50%,rgba(0,0,0,0.1),transparent_50%)] animate-pulse" />
      </div>
      
      <!-- Floating particles effect -->
      <div class="absolute inset-0 overflow-hidden pointer-events-none">
        <div class="absolute top-1/4 left-1/4 w-2 h-2 bg-primary-300/30 rounded-full animate-float" style="animation-delay: 0s; animation-duration: 6s;" />
        <div class="absolute top-1/3 right-1/4 w-3 h-3 bg-primary-400/20 rounded-full animate-float" style="animation-delay: 2s; animation-duration: 8s;" />
        <div class="absolute bottom-1/4 left-1/3 w-2 h-2 bg-primary-200/30 rounded-full animate-float" style="animation-delay: 4s; animation-duration: 7s;" />
      </div>

      <div class="container mx-auto px-4 md:px-6 lg:px-8 w-full relative z-10">
        <div
          ref="heroContentRef"
          class="max-w-3xl hero-content"
        >
          <h1 class="text-5xl md:text-6xl lg:text-7xl font-bold text-gray-900 mb-3 leading-tight hero-title-1">
            Stories & Inspiration.
          </h1>
          <h2 class="text-5xl md:text-6xl lg:text-7xl font-bold text-gray-900 mb-4 leading-tight hero-title-2">
            From Our Workshop.
          </h2>
          <p class="text-xl md:text-2xl lg:text-3xl font-medium text-gray-700 mb-10 hero-subtitle">
            Discover the art of handcrafted quilts and the stories behind each creation
          </p>
        </div>
      </div>

      <!-- Scroll Indicator -->
      <div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 animate-bounce">
        <div class="w-6 h-10 border-2 border-gray-400 rounded-full flex justify-center">
          <div class="w-1 h-3 bg-gray-400 rounded-full mt-2 animate-pulse" />
        </div>
      </div>
    </div>

    <!-- Blog Posts Section -->
    <section
      ref="blogSectionRef"
      class="py-20 md:py-32 bg-gradient-to-b from-white to-gray-50"
    >
      <div class="container mx-auto px-4 md:px-6 lg:px-8">
        <h2
          ref="sectionTitleRef"
          class="text-4xl md:text-5xl font-bold text-center text-gray-900 mb-4 section-title"
        >
          Latest Stories
        </h2>
        <p
          ref="sectionSubtitleRef"
          class="text-center text-gray-600 text-lg mb-16 max-w-2xl mx-auto section-subtitle"
        >
          Explore our blog for tips, tutorials, and stories about the art of quilting
        </p>
        
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 md:gap-8">
          <!-- Blog Post 1 -->
          <article
            ref="post1Ref"
            class="blog-card"
          >
            <UCard class="h-full transition-all duration-500 hover:shadow-2xl hover:-translate-y-2 border-0 shadow-lg group overflow-hidden">
              <template #header>
                <div class="aspect-video overflow-hidden rounded-t-lg relative group-hover:scale-105 transition-transform duration-500">
                  <div class="absolute inset-0 bg-gradient-to-t from-black/20 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 z-10" />
                  <NuxtImg
                    src="/quilt.png"
                    alt="The Art of Hand Stitching"
                    class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110"
                  />
                </div>
              </template>
              
              <div class="p-6">
                <div class="flex items-center gap-3 mb-3">
                  <span class="text-sm font-medium text-primary-600">Quilting Tips</span>
                  <span class="text-gray-400">•</span>
                  <span class="text-sm text-gray-500">March 15, 2024</span>
                </div>
                <h3 class="text-2xl font-bold text-gray-900 mb-3 group-hover:text-primary-600 transition-colors duration-300">
                  The Art of Hand Stitching
                </h3>
                <p class="text-gray-600 mb-4 line-clamp-3">
                  Discover the timeless techniques of hand stitching that have been passed down through generations. Learn how to create beautiful, durable quilts with traditional methods.
                </p>
              </div>
              
              <template #footer>
                <div class="p-6 pt-0">
                  <UButton
                    color="primary"
                    variant="ghost"
                    class="w-full rounded-lg transition-all duration-300 transform hover:scale-105"
                  >
                    Read More →
                  </UButton>
                </div>
              </template>
            </UCard>
          </article>

          <!-- Blog Post 2 -->
          <article
            ref="post2Ref"
            class="blog-card"
            style="animation-delay: 0.1s"
          >
            <UCard class="h-full transition-all duration-500 hover:shadow-2xl hover:-translate-y-2 border-0 shadow-lg group overflow-hidden">
              <template #header>
                <div class="aspect-video overflow-hidden rounded-t-lg relative group-hover:scale-105 transition-transform duration-500">
                  <div class="absolute inset-0 bg-gradient-to-t from-black/20 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 z-10" />
                  <NuxtImg
                    src="/quilt.png"
                    alt="Choosing the Perfect Fabric"
                    class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110"
                  />
                </div>
              </template>
              
              <div class="p-6">
                <div class="flex items-center gap-3 mb-3">
                  <span class="text-sm font-medium text-primary-600">Fabric Guide</span>
                  <span class="text-gray-400">•</span>
                  <span class="text-sm text-gray-500">March 8, 2024</span>
                </div>
                <h3 class="text-2xl font-bold text-gray-900 mb-3 group-hover:text-primary-600 transition-colors duration-300">
                  Choosing the Perfect Fabric
                </h3>
                <p class="text-gray-600 mb-4 line-clamp-3">
                  A comprehensive guide to selecting the right fabrics for your quilting projects. From cotton to linen, learn which materials work best for different quilt styles.
                </p>
              </div>
              
              <template #footer>
                <div class="p-6 pt-0">
                  <UButton
                    color="primary"
                    variant="ghost"
                    class="w-full rounded-lg transition-all duration-300 transform hover:scale-105"
                  >
                    Read More →
                  </UButton>
                </div>
              </template>
            </UCard>
          </article>

          <!-- Blog Post 3 -->
          <article
            ref="post3Ref"
            class="blog-card"
            style="animation-delay: 0.2s"
          >
            <UCard class="h-full transition-all duration-500 hover:shadow-2xl hover:-translate-y-2 border-0 shadow-lg group overflow-hidden">
              <template #header>
                <div class="aspect-video overflow-hidden rounded-t-lg relative group-hover:scale-105 transition-transform duration-500">
                  <div class="absolute inset-0 bg-gradient-to-t from-black/20 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 z-10" />
                  <NuxtImg
                    src="/quilt.png"
                    alt="Modern Quilt Patterns"
                    class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110"
                  />
                </div>
              </template>
              
              <div class="p-6">
                <div class="flex items-center gap-3 mb-3">
                  <span class="text-sm font-medium text-primary-600">Patterns</span>
                  <span class="text-gray-400">•</span>
                  <span class="text-sm text-gray-500">March 1, 2024</span>
                </div>
                <h3 class="text-2xl font-bold text-gray-900 mb-3 group-hover:text-primary-600 transition-colors duration-300">
                  Modern Quilt Patterns
                </h3>
                <p class="text-gray-600 mb-4 line-clamp-3">
                  Explore contemporary quilt patterns that blend traditional craftsmanship with modern design aesthetics. Get inspired by innovative approaches to classic techniques.
                </p>
              </div>
              
              <template #footer>
                <div class="p-6 pt-0">
                  <UButton
                    color="primary"
                    variant="ghost"
                    class="w-full rounded-lg transition-all duration-300 transform hover:scale-105"
                  >
                    Read More →
                  </UButton>
                </div>
              </template>
            </UCard>
          </article>

          <!-- Blog Post 4 -->
          <article
            ref="post4Ref"
            class="blog-card"
            style="animation-delay: 0.3s"
          >
            <UCard class="h-full transition-all duration-500 hover:shadow-2xl hover:-translate-y-2 border-0 shadow-lg group overflow-hidden">
              <template #header>
                <div class="aspect-video overflow-hidden rounded-t-lg relative group-hover:scale-105 transition-transform duration-500">
                  <div class="absolute inset-0 bg-gradient-to-t from-black/20 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 z-10" />
                  <NuxtImg
                    src="/quilt.png"
                    alt="Caring for Your Quilt"
                    class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110"
                  />
                </div>
              </template>
              
              <div class="p-6">
                <div class="flex items-center gap-3 mb-3">
                  <span class="text-sm font-medium text-primary-600">Care Guide</span>
                  <span class="text-gray-400">•</span>
                  <span class="text-sm text-gray-500">February 22, 2024</span>
                </div>
                <h3 class="text-2xl font-bold text-gray-900 mb-3 group-hover:text-primary-600 transition-colors duration-300">
                  Caring for Your Quilt
                </h3>
                <p class="text-gray-600 mb-4 line-clamp-3">
                  Essential tips for maintaining and preserving your handcrafted quilts. Learn proper cleaning, storage, and care techniques to keep your quilts beautiful for generations.
                </p>
              </div>
              
              <template #footer>
                <div class="p-6 pt-0">
                  <UButton
                    color="primary"
                    variant="ghost"
                    class="w-full rounded-lg transition-all duration-300 transform hover:scale-105"
                  >
                    Read More →
                  </UButton>
                </div>
              </template>
            </UCard>
          </article>

          <!-- Blog Post 5 -->
          <article
            ref="post5Ref"
            class="blog-card"
            style="animation-delay: 0.4s"
          >
            <UCard class="h-full transition-all duration-500 hover:shadow-2xl hover:-translate-y-2 border-0 shadow-lg group overflow-hidden">
              <template #header>
                <div class="aspect-video overflow-hidden rounded-t-lg relative group-hover:scale-105 transition-transform duration-500">
                  <div class="absolute inset-0 bg-gradient-to-t from-black/20 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 z-10" />
                  <NuxtImg
                    src="/quilt.png"
                    alt="The History of Quilting"
                    class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110"
                  />
                </div>
              </template>
              
              <div class="p-6">
                <div class="flex items-center gap-3 mb-3">
                  <span class="text-sm font-medium text-primary-600">History</span>
                  <span class="text-gray-400">•</span>
                  <span class="text-sm text-gray-500">February 15, 2024</span>
                </div>
                <h3 class="text-2xl font-bold text-gray-900 mb-3 group-hover:text-primary-600 transition-colors duration-300">
                  The History of Quilting
                </h3>
                <p class="text-gray-600 mb-4 line-clamp-3">
                  Journey through the rich history of quilting, from ancient civilizations to modern times. Discover how this craft has evolved and remained a beloved art form.
                </p>
              </div>
              
              <template #footer>
                <div class="p-6 pt-0">
                  <UButton
                    color="primary"
                    variant="ghost"
                    class="w-full rounded-lg transition-all duration-300 transform hover:scale-105"
                  >
                    Read More →
                  </UButton>
                </div>
              </template>
            </UCard>
          </article>

          <!-- Blog Post 6 -->
          <article
            ref="post6Ref"
            class="blog-card"
            style="animation-delay: 0.5s"
          >
            <UCard class="h-full transition-all duration-500 hover:shadow-2xl hover:-translate-y-2 border-0 shadow-lg group overflow-hidden">
              <template #header>
                <div class="aspect-video overflow-hidden rounded-t-lg relative group-hover:scale-105 transition-transform duration-500">
                  <div class="absolute inset-0 bg-gradient-to-t from-black/20 to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 z-10" />
                  <NuxtImg
                    src="/quilt.png"
                    alt="Quilting as Meditation"
                    class="w-full h-full object-cover transition-transform duration-700 group-hover:scale-110"
                  />
                </div>
              </template>
              
              <div class="p-6">
                <div class="flex items-center gap-3 mb-3">
                  <span class="text-sm font-medium text-primary-600">Wellness</span>
                  <span class="text-gray-400">•</span>
                  <span class="text-sm text-gray-500">February 8, 2024</span>
                </div>
                <h3 class="text-2xl font-bold text-gray-900 mb-3 group-hover:text-primary-600 transition-colors duration-300">
                  Quilting as Meditation
                </h3>
                <p class="text-gray-600 mb-4 line-clamp-3">
                  Discover the therapeutic benefits of quilting. Learn how this mindful craft can reduce stress, improve focus, and bring a sense of peace and accomplishment.
                </p>
              </div>
              
              <template #footer>
                <div class="p-6 pt-0">
                  <UButton
                    color="primary"
                    variant="ghost"
                    class="w-full rounded-lg transition-all duration-300 transform hover:scale-105"
                  >
                    Read More →
                  </UButton>
                </div>
              </template>
            </UCard>
          </article>
        </div>
      </div>
    </section>
  </div>
</template>

<script setup lang="ts">
const heroRef = ref<HTMLElement | null>(null)
const heroContentRef = ref<HTMLElement | null>(null)
const blogSectionRef = ref<HTMLElement | null>(null)
const sectionTitleRef = ref<HTMLElement | null>(null)
const sectionSubtitleRef = ref<HTMLElement | null>(null)
const post1Ref = ref<HTMLElement | null>(null)
const post2Ref = ref<HTMLElement | null>(null)
const post3Ref = ref<HTMLElement | null>(null)
const post4Ref = ref<HTMLElement | null>(null)
const post5Ref = ref<HTMLElement | null>(null)
const post6Ref = ref<HTMLElement | null>(null)

// Parallax effect for hero background
onMounted(() => {
  const handleScroll = () => {
    if (heroRef.value) {
      const scrolled = window.pageYOffset
      const rate = scrolled * 0.3
      const heroContent = heroContentRef.value
      
      // Subtle parallax on content
      if (heroContent && scrolled < 600) {
        heroContent.style.transform = `translateY(${rate}px)`
        heroContent.style.opacity = `${1 - scrolled / 600}`
      }
    }
  }

  window.addEventListener('scroll', handleScroll, { passive: true })

  // Intersection Observer for animations
  const observerOptions = {
    threshold: 0.1,
    rootMargin: '0px 0px -50px 0px'
  }

  const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry) => {
      if (entry.isIntersecting) {
        entry.target.classList.add('animate-in')
        observer.unobserve(entry.target)
      }
    })
  }, observerOptions)

  // Observe elements
  const elementsToObserve = [
    heroContentRef.value,
    sectionTitleRef.value,
    sectionSubtitleRef.value,
    post1Ref.value,
    post2Ref.value,
    post3Ref.value,
    post4Ref.value,
    post5Ref.value,
    post6Ref.value
  ]

  elementsToObserve.forEach((el) => {
    if (el) observer.observe(el)
  })

  // Initial hero animation
  nextTick(() => {
    if (heroContentRef.value) {
      heroContentRef.value.classList.add('animate-in')
    }
  })

  onUnmounted(() => {
    window.removeEventListener('scroll', handleScroll)
  })
})
</script>

<style scoped>
/* Hero Animations */
.hero-content {
  opacity: 0;
  transform: translateY(30px);
  transition: opacity 1s ease-out, transform 1s ease-out;
}

.hero-content.animate-in {
  opacity: 1;
  transform: translateY(0);
}

.hero-title-1 {
  opacity: 0;
  transform: translateX(-50px);
  animation: slideInLeft 0.8s ease-out 0.2s forwards;
}

.hero-title-2 {
  opacity: 0;
  transform: translateX(-50px);
  animation: slideInLeft 0.8s ease-out 0.4s forwards;
}

.hero-subtitle {
  opacity: 0;
  transform: translateY(20px);
  animation: fadeInUp 0.8s ease-out 0.6s forwards;
}

/* Section Animations */
.section-title {
  opacity: 0;
  transform: translateY(30px);
  transition: opacity 0.8s ease-out, transform 0.8s ease-out;
}

.section-title.animate-in {
  opacity: 1;
  transform: translateY(0);
}

.section-subtitle {
  opacity: 0;
  transform: translateY(20px);
  transition: opacity 0.8s ease-out, transform 0.8s ease-out;
}

.section-subtitle.animate-in {
  opacity: 1;
  transform: translateY(0);
  transition-delay: 0.2s;
}

/* Blog Card Animations */
.blog-card {
  opacity: 0;
  transform: translateY(50px) scale(0.95);
  transition: opacity 0.6s ease-out, transform 0.6s ease-out;
}

.blog-card.animate-in {
  opacity: 1;
  transform: translateY(0) scale(1);
}

/* Enhanced hover effects for cards */
.blog-card:hover {
  transform: translateY(-8px) scale(1.02);
}

/* Keyframe Animations */
@keyframes slideInLeft {
  from {
    opacity: 0;
    transform: translateX(-50px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes float {
  0%, 100% {
    transform: translateY(0px) translateX(0px);
    opacity: 0.3;
  }
  25% {
    transform: translateY(-20px) translateX(10px);
    opacity: 0.5;
  }
  50% {
    transform: translateY(-30px) translateX(-5px);
    opacity: 0.4;
  }
  75% {
    transform: translateY(-15px) translateX(5px);
    opacity: 0.5;
  }
}

/* Smooth scrolling */
:global(html) {
  scroll-behavior: smooth;
}

/* Hero section parallax container */
.hero-section {
  will-change: transform;
  background-attachment: fixed;
}

/* Additional polish */
.blog-card :deep(.card) {
  transition: all 0.5s cubic-bezier(0.4, 0, 0.2, 1);
}

/* Image zoom effect on hover */
.blog-card :deep(img) {
  transition: transform 0.7s cubic-bezier(0.4, 0, 0.2, 1);
}

/* Responsive adjustments */
@media (max-width: 768px) {
  .hero-section {
    background-attachment: scroll;
  }
}
</style>

