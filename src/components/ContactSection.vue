<script setup>
import { Mail, MapPin, Phone } from 'lucide-vue-next';
</script>

<template>
  <section id="contact" class="py-20 bg-slate-900/50">
    <div class="container mx-auto px-6">
      <div class="max-w-4xl mx-auto">
        <div class="text-center mb-16">
          <h2 class="text-3xl font-bold mb-4 text-white">Get In Touch</h2>
          <p class="text-slate-400">Have a project in mind? Let's work together.</p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
          <div>
            <h3 class="text-xl font-semibold text-white mb-6">Contact Information</h3>
            <div class="space-y-6">
              <div class="flex items-start gap-4">
                <div class="p-3 bg-indigo-500/10 rounded-lg text-indigo-400">
                  <Mail class="w-6 h-6" />
                </div>
                <div>
                  <h4 class="text-white font-medium">Email</h4>
                  <p class="text-slate-400">firintech3@gmail.com</p>
                </div>
              </div>

              <div class="flex items-start gap-4">
                <div class="p-3 bg-indigo-500/10 rounded-lg text-indigo-400">
                  <Phone class="w-6 h-6" />
                </div>
                <div>
                  <h4 class="text-white font-medium">Phone</h4>
                  <p class="text-slate-400">+252907024306</p>
                </div>
              </div>

              <div class="flex items-start gap-4">
                <div class="p-3 bg-indigo-500/10 rounded-lg text-indigo-400">
                  <MapPin class="w-6 h-6" />
                </div>
                <div>
                  <h4 class="text-white font-medium">Location</h4>
                  <p class="text-slate-400">Puntland, Somalia</p>
                </div>
              </div>
            </div>
          </div>

          <form class="space-y-4" @submit.prevent>
            <div>
              <input type="text" placeholder="Your Name"
                class="w-full px-4 py-3 bg-slate-800 border border-slate-700 rounded-lg focus:outline-none focus:border-indigo-500 text-white placeholder-slate-500 transition-colors" />
            </div>
            <div>
              <input type="email" placeholder="Your Email"
                class="w-full px-4 py-3 bg-slate-800 border border-slate-700 rounded-lg focus:outline-none focus:border-indigo-500 text-white placeholder-slate-500 transition-colors" />
            </div>
            <div>
              <textarea rows="4" placeholder="Your Message"
                class="w-full px-4 py-3 bg-slate-800 border border-slate-700 rounded-lg focus:outline-none focus:border-indigo-500 text-white placeholder-slate-500 transition-colors"></textarea>
            </div>
            <button
              class="w-full px-8 py-3 bg-indigo-600 hover:bg-indigo-700 text-white rounded-lg font-medium transition-colors">
              Send Message
            </button>
          </form>
        </div>
      </div>
    </div>
  </section>
</template>
