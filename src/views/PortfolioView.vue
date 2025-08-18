<template>
  <div class="container mx-auto p-3 md:p-8 min-h-screen relative overflow-hidden">
    <!-- Background decorative elements -->
    <div class="absolute inset-0 overflow-hidden pointer-events-none">
      <div class="floating-shape shape-1"></div>
      <div class="floating-shape shape-2"></div>
      <div class="floating-shape shape-3"></div>
      <div class="floating-shape shape-4"></div>
      <div class="floating-shape shape-5"></div>
    </div>
    
    <div class="max-w-7xl mx-auto relative z-10">
      <div class="fade-zoom-up">
        <!-- Header Section -->
        <div class="text-center mb-10 pt-4">
  <div class="inline-block mb-6">
    <div class="pulse-ring"></div>
    <div class="pulse-ring pulse-ring-delay"></div>
    <h1 class="text-4xl md:text-5xl font-bold bg-clip-text bg-gradient-to-r from-slate-100 via-amber-300 to-orange-400 text-transparent mb-6 animate-text-shine leading-normal py-2">
      My Project
    </h1>
  </div>
  <p class="text-slate-400 text-lg max-w-2xl mx-auto leading-relaxed mb-6">
    Various projects I have worked on using modern technologies
  </p>
  
  <!-- Decorative line -->
  <div class="flex items-center justify-center mb-8">
    <div class="h-px bg-gradient-to-r from-transparent via-amber-400 to-transparent w-32"></div>
    <div class="mx-4">
      <div class="w-2 h-2 bg-amber-400 rounded-full animate-pulse"></div>
    </div>
    <div class="h-px bg-gradient-to-r from-transparent via-amber-400 to-transparent w-32"></div>
  </div>

  <!-- Project count indicator -->
  <div class="inline-flex items-center px-6 py-3 bg-gradient-to-r from-amber-200/10 to-yellow-500/10 rounded-full border border-amber-200/20 backdrop-blur-sm">
    <svg class="w-5 h-5 text-amber-400 mr-2" fill="currentColor" viewBox="0 0 20 20">
      <path d="M3 4a1 1 0 011-1h12a1 1 0 011 1v2a1 1 0 01-1 1H4a1 1 0 01-1-1V4zM3 10a1 1 0 011-1h6a1 1 0 011 1v6a1 1 0 01-1 1H4a1 1 0 01-1-1v-6zM14 9a1 1 0 00-1 1v6a1 1 0 001 1h2a1 1 0 001-1v-6a1 1 0 00-1-1h-2z"/>
    </svg>
    <span class="text-amber-200 font-medium">{{ items.length }} Projects</span>
  </div>
</div>

        <!-- Projects Grid -->
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 md:gap-8">
          <div v-for="(item, index) in items" :key="item.id" 
               class="project-card group"
               :style="{ animationDelay: `${index * 200}ms` }">
            
            <div class="card-glow"></div>
            
            <!-- Project Card Content -->
            <div class="relative z-10 h-full">
              <!-- Project Image -->
              <div class="relative overflow-hidden rounded-t-xl mb-4">
                <div class="aspect-video bg-gradient-to-br from-amber-200/5 to-yellow-500/5 flex items-center justify-center">
                  <img 
                    :src="'/img/portfolio-' + item.imageUrl + '.png'"
                    :alt="item.name"
                    class="w-full h-full object-cover transition-all duration-500 group-hover:scale-110"
                    loading="lazy">
                  
                  <!-- Overlay on hover -->
                  <div class="absolute inset-0 bg-gradient-to-t from-black/60 via-transparent to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
                  
                  <!-- Project type badge -->
                  <div class="absolute top-3 left-3 px-3 py-1 bg-black/70 backdrop-blur-sm rounded-full">
                    <span class="text-xs text-amber-200 font-medium">Web App</span>
                  </div>
                </div>
              </div>

              <!-- Project Info -->
              <div class="px-6 pb-6">
                <!-- Project Title -->
                <h3 class="text-xl font-bold text-amber-200 mb-3 group-hover:text-amber-100 transition-colors">
                  {{ item.name }}
                </h3>
                
                <!-- Project Description -->
                <p class="text-slate-400 text-sm mb-4 leading-relaxed group-hover:text-slate-300 transition-colors line-clamp-3">
                  {{ item.status }}
                </p>
                
                <!-- Tech Stack -->
                <div class="mb-6">
                  <div class="flex items-center mb-2">
                    <svg class="w-4 h-4 text-amber-400 mr-2" fill="currentColor" viewBox="0 0 20 20">
                      <path d="M13 6a3 3 0 11-6 0 3 3 0 016 0zM18 8a2 2 0 11-4 0 2 2 0 014 0zM14 15a4 4 0 00-8 0v3h8v-3z"/>
                    </svg>
                    <span class="text-xs text-slate-500 font-medium uppercase tracking-wide">Tech Stack</span>
                  </div>
                  <div class="flex flex-wrap gap-2">
                    <span v-for="tech in item.tech.split(', ')" :key="tech"
                          class="px-2 py-1 bg-gradient-to-r from-amber-500/10 to-orange-500/10 text-amber-300 text-xs font-medium rounded-md border border-amber-500/20 transition-all duration-300 hover:border-amber-400/40 hover:bg-amber-500/20">
                      {{ tech }}
                    </span>
                  </div>
                </div>
                
                <!-- Action Buttons -->
                <div class="flex gap-3">
                  <!-- GitHub Button -->
                  <a :href="item.github" 
                     target="_blank" 
                     rel="noreferrer"
                     class="flex-1 group/btn flex items-center justify-center gap-2 px-4 py-3 bg-gradient-to-r from-slate-800 to-slate-900 hover:from-amber-600 hover:to-orange-600 text-slate-300 hover:text-white text-sm font-medium rounded-lg border border-slate-700 hover:border-amber-500/40 transition-all duration-300 hover:shadow-lg hover:shadow-amber-500/20 hover:-translate-y-1">
                    <svg class="w-4 h-4 transition-transform duration-300 group-hover/btn:scale-110" fill="currentColor" viewBox="0 0 24 24">
                      <path d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"/>
                    </svg>
                    <span>Github</span>
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeTab: 1,
      items: [
        {
          id: 1,
          name: 'Personal Website',
          imageUrl: 'personal',
          status: 'My personal website, I created this website to display my profile, skills and projects. As well as my place to try new technology.',
          tech: 'VueJS 3, Tailwind',
          github: 'https://github.com/TegarMallisa/my-personal-website'
        },
        {
          id: 2,
          name: 'SIGBARU',
          imageUrl: 'sigbaru',
          status: 'A warehouse information system that applies the FEFO method to control the flow of outgoing products in the warehouse.',
          tech: 'Nuxt 3, Tailwind, Express JS',
          github: 'https://github.com/TegarMallisa/frontend-sigbaru-petshop'
        },
        {
          id: 3,
          name: 'Big Military System',
          imageUrl: 'bms',
          status: 'A military reporting website designed to manage member data and streamline personnel reporting at each military base.',
          tech: 'Nuxt 3, Tailwind, Axios',
          github: 'https://github.com/TegarMallisa/babinsa-messenger-fe'
        },
      ]
    };
  },
  methods: {
  }
}
</script>

<style scoped>
/* Background decorative elements */
.floating-shape {
  position: absolute;
  border-radius: 50%;
  opacity: 0.08;
  animation: float 8s ease-in-out infinite;
}

.shape-1 {
  width: 120px;
  height: 120px;
  background: linear-gradient(45deg, #f59e0b, #f97316);
  top: 10%;
  left: 10%;
  animation-delay: 0s;
}

.shape-2 {
  width: 80px;
  height: 80px;
  background: linear-gradient(45deg, #3b82f6, #1d4ed8);
  top: 60%;
  right: 15%;
  animation-delay: 2s;
}

.shape-3 {
  width: 100px;
  height: 100px;
  background: linear-gradient(45deg, #10b981, #059669);
  bottom: 20%;
  left: 20%;
  animation-delay: 4s;
}

.shape-4 {
  width: 60px;
  height: 60px;
  background: linear-gradient(45deg, #8b5cf6, #7c3aed);
  top: 30%;
  right: 30%;
  animation-delay: 1s;
}

.shape-5 {
  width: 90px;
  height: 90px;
  background: linear-gradient(45deg, #ef4444, #dc2626);
  bottom: 40%;
  right: 10%;
  animation-delay: 3s;
}

@keyframes float {
  0%, 100% { transform: translateY(0px) rotate(0deg); }
  25% { transform: translateY(-20px) rotate(90deg); }
  50% { transform: translateY(-10px) rotate(180deg); }
  75% { transform: translateY(-15px) rotate(270deg); }
}

/* Pulse rings */
.pulse-ring {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 300px;
  height: 300px;
  border: 2px solid rgba(245, 158, 11, 0.3);
  border-radius: 50%;
  animation: pulse 3s infinite;
}

.pulse-ring-delay {
  animation-delay: 1.5s;
  border-color: rgba(245, 158, 11, 0.2);
  width: 400px;
  height: 400px;
}

@keyframes pulse {
  0% {
    transform: translate(-50%, -50%) scale(0.8);
    opacity: 1;
  }
  100% {
    transform: translate(-50%, -50%) scale(1.3);
    opacity: 0;
  }
}

/* Text shine animation */
@keyframes text-shine {
  0% { background-position: 0% 50%; }
  50% { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

.animate-text-shine {
  background-size: 200% auto;
  animation: text-shine 4s ease-in-out infinite;
}

/* Project cards */
.project-card {
  @apply bg-[#1e1e1f] border border-[#383838] rounded-xl hover:bg-[#262626] transition-all duration-500 cursor-pointer relative overflow-hidden h-full;
  opacity: 0;
  animation: slideInUp 0.8s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards;
  transform: translateY(0);
}

.project-card:hover {
  transform: translateY(-12px);
  box-shadow: 0 25px 30px -5px rgba(0, 0, 0, 0.4), 0 15px 15px -5px rgba(0, 0, 0, 0.2);
  border-color: rgba(245, 158, 11, 0.4);
}

.card-glow {
  position: absolute;
  inset: 0;
  background: linear-gradient(45deg, rgba(245, 158, 11, 0.05), rgba(249, 115, 22, 0.05));
  opacity: 0;
  transition: opacity 0.5s ease;
  border-radius: inherit;
}

.project-card:hover .card-glow {
  opacity: 1;
}

/* Animations */
@keyframes slideInUp {
  from {
    opacity: 0;
    transform: translateY(60px) scale(0.9);
  }
  to {
    opacity: 1;
    transform: translateY(0) scale(1);
  }
}

@keyframes fadeZoomUp {
  0% {
    opacity: 0;
    transform: scale(0.9) translateY(40px);
  }
  100% {
    opacity: 1;
    transform: scale(1) translateY(0);
  }
}

.fade-zoom-up {
  animation: fadeZoomUp 1.2s cubic-bezier(0.25, 0.46, 0.45, 0.94);
}

/* Text line clamping */
.line-clamp-3 {
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
  overflow: hidden;
}

/* Responsive improvements */
@media (max-width: 768px) {
  .project-card {
    margin-bottom: 1rem;
  }
  
  .project-card:hover {
    transform: translateY(-8px);
  }
  
  .floating-shape {
    opacity: 0.04;
  }
  
  .pulse-ring {
    width: 200px;
    height: 200px;
  }
  
  .pulse-ring-delay {
    width: 250px;
    height: 250px;
  }
}

/* Enhanced button hover effects */
.group\/btn:hover {
  transform: translateY(-1px);
}

.group\/view:hover {
  transform: translateY(-1px);
}

/* Smooth transitions */
* {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>