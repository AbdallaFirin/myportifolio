<script setup>
import { ArrowRight } from 'lucide-vue-next';
</script>

<template>
  <section id="hero" class="min-h-screen flex items-center justify-center relative overflow-hidden pt-16">
    <!-- Background Elements -->
    <div class="absolute top-0 left-0 w-full h-full overflow-hidden -z-10">
      <div class="absolute top-[-10%] left-[-10%] w-96 h-96 bg-indigo-500/20 rounded-full blur-3xl animate-pulse"></div>
      <div
        class="absolute bottom-[-10%] right-[-10%] w-96 h-96 bg-cyan-500/20 rounded-full blur-3xl animate-pulse delay-1000">
      </div>
    </div>

    <div class="container mx-auto px-6 text-center z-10">
      <h2 class="text-indigo-400 font-medium tracking-wider mb-4 animate-fade-in-up">HELLO, I'M</h2>
      <h1
        class="text-5xl md:text-7xl font-bold mb-6 bg-clip-text text-transparent bg-gradient-to-r from-white to-slate-400 animate-fade-in-up delay-100">
        Abdalla Firin
      </h1>
      <p class="text-xl md:text-2xl text-slate-400 mb-8 max-w-2xl mx-auto animate-fade-in-up delay-200">
        Full Stack Developer building impactful digital solutions. </p>

      <div class="flex flex-col md:flex-row gap-4 justify-center items-center animate-fade-in-up delay-300">
        <a href="#projects"
          class="group relative px-8 py-3 bg-indigo-600 hover:bg-indigo-700 text-white rounded-full font-medium transition-all duration-300 hover:shadow-lg hover:shadow-indigo-500/30 flex items-center gap-2">
          View Work
          <ArrowRight class="w-4 h-4 group-hover:translate-x-1 transition-transform" />
        </a>
        <a href="#contact"
          class="px-8 py-3 border border-slate-700 hover:border-slate-500 text-slate-300 hover:text-white rounded-full font-medium transition-all duration-300">
          Contact Me
        </a>
      </div>
    </div>
  </section>
</template>

<style scoped>
.animate-fade-in-up {
  animation: fadeInUp 0.8s ease-out forwards;
  opacity: 0;
  transform: translateY(20px);
}

.delay-100 {
  animation-delay: 0.1s;
}

.delay-200 {
  animation-delay: 0.2s;
}

.delay-300 {
  animation-delay: 0.3s;
}

@keyframes fadeInUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
