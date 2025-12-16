<script setup>
import { ExternalLink, Github } from 'lucide-vue-next';

const projects = [
  {
    title: 'E-book Website',
    desc: 'E-Book Website built with Bootstrap, Sass, and JavaScript.',
    tags: ['Bootstrap', 'Sass', 'JavaScript'],
    image: 'https://images.unsplash.com/photo-1532012197267-da84d127e765?ixlib=rb-4.0.3&auto=format&fit=crop&w=1000&q=80',
    link: 'https://e-book-website-2ybd-git-main-abdalla-firins-projects.vercel.app/',
    github: 'https://github.com/AbdallaFirin/E-book-Website'
  },
  {
    title: 'Course Training Website',
    desc: 'A platform for online course training and education.',
    tags: ['Web Dev', 'Education', 'Frontend'],
    image: 'https://images.unsplash.com/photo-1501504905252-473c47e087f8?ixlib=rb-4.0.3&auto=format&fit=crop&w=1000&q=80',
    link: 'https://github.com/AbdallaFirin/CourseTraning-Website',
    github: 'https://github.com/AbdallaFirin/CourseTraning-Website'
  },
  {
    title: 'Course Training Website',
    desc: 'A platform for online course training and education.',
    tags: ['Web Dev', 'Education', 'Frontend'],
    image: 'https://images.unsplash.com/photo-1501504905252-473c47e087f8?ixlib=rb-4.0.3&auto=format&fit=crop&w=1000&q=80',
    link: 'https://github.com/AbdallaFirin/CourseTraning-Website',
    github: 'https://github.com/AbdallaFirin/CourseTraning-Website'
  }
];
</script>

<template>
  <section id="projects" class="py-20">
    <div class="container mx-auto px-6">
      <div class="text-center mb-16">
        <h2 class="text-3xl font-bold mb-4 text-white">Featured Projects</h2>
        <p class="text-slate-400 max-w-2xl mx-auto">Here are some of the projects I've worked on recently.</p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div v-for="(project, index) in projects" :key="index"
          class="group bg-slate-800 rounded-2xl overflow-hidden border border-slate-700 hover:border-indigo-500/50 transition-all duration-300 hover:-translate-y-2 hover:shadow-xl hover:shadow-indigo-500/10">
          <div class="relative h-48 overflow-hidden">
            <div class="absolute inset-0 bg-slate-900/20 group-hover:bg-transparent transition-colors z-10"></div>
            <img :src="project.image" :alt="project.title"
              class="w-full h-full object-cover transform group-hover:scale-110 transition-transform duration-500" />
          </div>
          <div class="p-6">
            <div class="flex gap-2 mb-4">
              <span v-for="tag in project.tags" :key="tag"
                class="px-3 py-1 text-xs font-medium bg-indigo-500/10 text-indigo-400 rounded-full">
                {{ tag }}
              </span>
            </div>

            <h3 class="text-xl font-bold text-white mb-2">{{ project.title }}</h3>
            <p class="text-slate-400 mb-6 text-sm">{{ project.desc }}</p>

            <div class="flex items-center gap-4">
              <a :href="project.link"
                class="flex items-center gap-2 text-sm font-medium text-white hover:text-indigo-400 transition-colors">
                <ExternalLink class="w-4 h-4" /> Live Demo
              </a>
              <a :href="project.github"
                class="flex items-center gap-2 text-sm font-medium text-slate-400 hover:text-white transition-colors">
                <Github class="w-4 h-4" /> Code
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
