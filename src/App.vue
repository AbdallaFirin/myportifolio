<script setup>
import { ref, onMounted, onUnmounted } from 'vue';
import { Menu, X, Github, Linkedin, Twitter } from 'lucide-vue-next';
import HeroSection from './components/HeroSection.vue';
import AboutSection from './components/AboutSection.vue';
import ProjectsSection from './components/ProjectsSection.vue';
import ContactSection from './components/ContactSection.vue';

const isMenuOpen = ref(false);
const isScrolled = ref(false);

const checkScroll = () => {
  isScrolled.value = window.scrollY > 50;
};

onMounted(() => {
  window.addEventListener('scroll', checkScroll);
});

onUnmounted(() => {
  window.removeEventListener('scroll', checkScroll);
});

const navLinks = [
  { name: 'Home', href: '#hero' },
  { name: 'About', href: '#about' },
  { name: 'Projects', href: '#projects' },
  { name: 'Contact', href: '#contact' },
];
</script>

<template>
  <div class="min-h-screen bg-slate-900 text-slate-100 selection:bg-indigo-500/30">
    <!-- Navbar -->
    <nav
      :class="['fixed top-0 w-full z-50 transition-all duration-300', isScrolled ? 'glass-nav py-4' : 'bg-transparent py-6']">
      <div class="container mx-auto px-6 flex justify-between items-center">
        <a href="#"
          class="text-2xl font-bold bg-clip-text text-transparent bg-gradient-to-r from-indigo-400 to-cyan-400">
          FirinTec.
        </a>

        <!-- Desktop Menu -->
        <div class="hidden md:flex items-center gap-8">
          <a v-for="link in navLinks" :key="link.name" :href="link.href"
            class="text-sm font-medium text-slate-300 hover:text-white transition-colors">
            {{ link.name }}
          </a>
          <a href="#contact"
            class="px-5 py-2 bg-indigo-600 hover:bg-indigo-700 text-white rounded-full text-sm font-medium transition-colors">
            Hire Me
          </a>
        </div>

        <!-- Mobile Menu Button -->
        <button @click="isMenuOpen = !isMenuOpen" class="md:hidden text-white">
          <Menu v-if="!isMenuOpen" class="w-6 h-6" />
          <X v-else class="w-6 h-6" />
        </button>
      </div>

      <!-- Mobile Menu -->
      <div v-if="isMenuOpen"
        class="md:hidden absolute top-full left-0 w-full bg-slate-900 border-b border-slate-800 p-6 flex flex-col gap-4 shadow-xl">
        <a v-for="link in navLinks" :key="link.name" :href="link.href" @click="isMenuOpen = false"
          class="text-slate-300 hover:text-white font-medium">
          {{ link.name }}
        </a>
      </div>
    </nav>

    <main>
      <HeroSection />
      <AboutSection />
      <ProjectsSection />
      <ContactSection />
    </main>

    <footer class="bg-slate-950 py-12 border-t border-slate-900">
      <div class="container mx-auto px-6 flex flex-col md:flex-row justify-between items-center gap-6">
        <div class="text-slate-400 text-sm">
          © {{ new Date().getFullYear() }} AbdallaFirin. All rights reserved.
        </div>

        <div class="flex items-center gap-6">
          <a href="https://github.com/AbdallaFirin" class="text-slate-400 hover:text-white transition-colors">
            <Github class="w-5 h-5" />
          </a>
          <a href="https://www.linkedin.com/in/abdalla-firin-said-b1653b219/"
            class="text-slate-400 hover:text-white transition-colors">
            <Linkedin class="w-5 h-5" />
          </a>
          <a href="#" class="text-slate-400 hover:text-white transition-colors">
            <Twitter class="w-5 h-5" />
          </a>
        </div>
      </div>
    </footer>
  </div>
</template>
