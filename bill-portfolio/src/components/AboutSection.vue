
<template>
  <section id="about" class="section-padding bg-gray-50 dark:bg-gray-800">
    <div class="max-w-7xl mx-auto">
      <div class="text-center mb-12">
        <h2 class="text-3xl md:text-4xl font-bold text-gray-900 dark:text-white mb-4">
          À propos de moi
        </h2>
        <p class="text-gray-600 dark:text-gray-300 max-w-2xl mx-auto">
          Découvrez mon parcours et ma passion pour le développement
        </p>
      </div>
      
      <div class="grid md:grid-cols-2 gap-12 items-center">
        <div class="animate-slide-up">
          <div class="aspect-square bg-gradient-to-br from-primary-400 to-primary-600 rounded-2xl flex items-center justify-center text-white text-6xl font-bold">
            {{ initials }}
          </div>
        </div>
        
        <div class="animate-slide-up">
          <h3 class="text-2xl font-bold text-gray-900 dark:text-white mb-4">
            Passionné par la technologie
          </h3>
          <p class="text-gray-600 dark:text-gray-300 mb-6 leading-relaxed">
            Je suis un développeur full-stack avec une passion pour la création d'applications web modernes et performantes. 
            Avec plusieurs années d'expérience dans le développement, j'aime transformer des idées complexes en solutions élégantes et intuitives.
          </p>
          <p class="text-gray-600 dark:text-gray-300 mb-8 leading-relaxed">
            Mon expertise couvre les technologies front-end et back-end, avec une attention particulière portée à l'expérience utilisateur 
            et aux bonnes pratiques de développement.
          </p>
          
          <div class="flex flex-wrap gap-3">
            <span v-for="interest in interests" :key="interest" 
                  class="px-3 py-1 bg-primary-100 dark:bg-primary-900 text-primary-800 dark:text-primary-200 rounded-full text-sm font-medium">
              {{ interest }}
            </span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const initials = ref('VN') // À personnaliser avec vos initiales
const interests = ref([
  'Développement Web',
  'UI/UX Design',
  'Technologies Open Source',
  'Intelligence Artificielle',
  'Performance Web'
])
</script>
