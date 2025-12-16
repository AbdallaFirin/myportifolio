<script setup>
import { Code, Palette, Terminal, Database } from 'lucide-vue-next';
import profileImage from '../assets/image/WhatsApp Image 2025-09-05 at 17.49.06.jpeg';

const skills = [
    { name: 'Frontend', icon: Code, desc: 'React, Vue, Tailwind, JS' },
    { name: 'Backend', icon: Terminal, desc: 'Laravel, Node.js, PHP, Python' },
    { name: 'Database', icon: Database, desc: 'MySQL, MongoDB' },
];
</script>

<template>
    <section id="about" class="py-20 bg-slate-900/50">
        <div class="container mx-auto px-6">
            <div class="flex flex-col md:flex-row items-center gap-12">

                <div class="w-full md:w-1/2">
                    <h2 class="text-3xl font-bold mb-6 text-white">About Me</h2>
                    <p class="text-slate-400 mb-4 leading-relaxed">
                        I'm a dedicated Full Stack Developer with a strong focus on creating clean, efficient, and
                        user-friendly web applications. I work with technologies such as JavaScript, PHP, Laravel,
                        Python, React, Node.js, MySQL, and Express, and I'm especially passionate about building
                        powerful backend systems using Laravel.
                    </p>
                    <p class="text-slate-400 mb-4 leading-relaxed">
                        Alongside development, I've also built skills in digital marketing — including Facebook
                        marketing, email marketing, and content creation. This combination of technical and marketing
                        experience helps me build solutions that are not only functional but also impactful and
                        user-oriented.
                    </p>
                    <p class="text-slate-400 mb-8 leading-relaxed">
                        My goal is to keep improving, build meaningful digital products, and contribute to projects that
                        make a real difference.
                    </p>

                    <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                        <div v-for="skill in skills" :key="skill.name"
                            class="p-4 bg-slate-800/50 rounded-xl border border-slate-700/50 hover:border-indigo-500/50 transition-colors">
                            <component :is="skill.icon" class="w-6 h-6 text-indigo-400 mb-2" />
                            <h3 class="text-white font-medium">{{ skill.name }}</h3>
                            <p class="text-sm text-slate-500">{{ skill.desc }}</p>
                        </div>
                    </div>
                </div>

                <div class="w-full md:w-1/2">
                    <div class="relative">
                        <img :src="profileImage" alt="Profile"
                            class="w-full max-w-md mx-auto shadow-lg hover:grayscale hover:scale-105 transition-all duration-500" />
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
