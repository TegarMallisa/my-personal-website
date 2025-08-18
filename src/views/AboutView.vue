<script>
export default {
  data() {
    return {
      activeTab: 1,
      tech: [
        {
          id: 1,
          name: 'HTML',
          imageUrl: 'https://cdn-icons-png.flaticon.com/512/1051/1051277.png',
          status: 'Advanced',
          level: 95
        },
        {
          id: 2,
          name: 'CSS',
          imageUrl: 'https://cdn-icons-png.flaticon.com/512/732/732190.png',
          status: 'Advanced',
          level: 90
        },
        {
          id: 3,
          name: 'Javascript',
          imageUrl: 'https://cdn.icon-icons.com/icons2/2415/PNG/512/javascript_original_logo_icon_146455.png',
          status: 'Advanced',
          level: 88
        },
        {
          id: 4,
          name: 'Tailwind',
          imageUrl: 'https://upload.wikimedia.org/wikipedia/commons/d/d5/Tailwind_CSS_Logo.svg',
          status: 'Advanced',
          level: 85
        },
        {
          id: 5,
          name: 'NuxtJS',
          imageUrl: require('@/assets/images/nuxt.svg'),
          status: 'Intermediate',
          level: 75
        },
        {
          id: 6,
          name: 'NodeJS',
          imageUrl: 'https://cdn.iconscout.com/icon/free/png-256/free-node-js-1174925.png',
          status: 'Intermediate',
          level: 70
        },
        {
          id: 7,
          name: 'PHP',
          imageUrl: 'https://cdn.iconscout.com/icon/free/png-256/free-php-2038871-1720084.png',
          status: 'Beginner',
          level: 50
        },
        {
          id: 8,
          name: 'Laravel',
          imageUrl: 'https://cdn.worldvectorlogo.com/logos/laravel-2.svg',
          status: 'Beginner',
          level: 45
        }
      ],
      tools: [
        {
          id: 1,
          name: 'Git',
          imageUrl: 'https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png',
          status: 'Version Control',
          level: 85
        },
        {
          id: 2,
          name: 'GitHub',
          imageUrl: 'https://cdn-icons-png.flaticon.com/512/25/25231.png',
          status: 'Git Hosting',
          level: 90
        },
        {
          id: 3,
          name: 'NPM',
          imageUrl: 'https://cdn.iconscout.com/icon/free/png-256/free-npm-3-1175132.png',
          status: 'Package Manager',
          level: 80
        },
        {
          id: 4,
          name: 'MySQL',
          imageUrl: 'https://cdn-icons-png.flaticon.com/512/5968/5968313.png',
          status: 'Database',
          level: 85
        },
        {
          id: 5,
          name: 'Figma',
          imageUrl: require('@/assets/images/figma.svg'),
          status: 'Design',
          level: 85
        },
        {
          id: 6,
          name: 'Postman',
          imageUrl: require('@/assets/images/postman.svg'),
          status: 'API Testing',
          level: 85
        },
      ]
    };
  },
      methods: {
    getStatusColor(status) {
      const colors = {
        'Advanced': 'text-green-400',
        'Intermediate': 'text-yellow-400',
        'Beginner': 'text-red-400',
        'Version Control': 'text-indigo-400',
        'Git Hosting': 'text-indigo-400',
        'Package Manager': 'text-indigo-400',
        'Database': 'text-indigo-400',
        'Design': 'text-indigo-400',
        'API Testing': 'text-indigo-400'
      };
      return colors[status] || 'text-amber-200';
    }
  }
}
</script>

<template>
  <!-- About Me Section -->
  <div
    class="relative bg-gradient-to-br from-[#1e1e1f] via-[#252526] to-[#1e1e1f] px-6 py-8 md:px-12 md:py-12 text-left border border-[#383838] rounded-3xl text-amber-50 mx-3 mb-8 shadow-2xl overflow-hidden">
    
    <!-- Background decorative elements -->
    <div class="absolute inset-0 overflow-hidden pointer-events-none">
      <div class="absolute top-10 right-10 w-40 h-40 bg-amber-200/5 rounded-full blur-3xl animate-pulse"></div>
      <div class="absolute bottom-20 left-10 w-32 h-32 bg-yellow-500/5 rounded-full blur-2xl animate-float"></div>
    </div>

    <article data-page="about" class="relative z-10">
      <header>
        <div class="text-3xl font-bold text-white mb-8 fadein-bot title-section flex items-center">
          <span class="bg-gradient-to-r from-amber-200 to-yellow-500 bg-clip-text text-transparent mr-4">About Me</span>
          <div class="h-[2px] flex-1 bg-gradient-to-r from-amber-200 via-yellow-500 to-transparent rounded-full aos-init aos-animate" 
               data-aos="zoom-in-left" data-aos-duration="600"></div>
        </div>
      </header>

      <section class="text-base md:text-lg text-justify flex flex-col gap-6 md:flex-row md:gap-12 md:justify-left md:items-start">
        <!-- Profile Image Section -->
        <div class="flex justify-center md:w-5/12 lg:w-4/12">
          <div class="relative group">
            <!-- Decorative rings -->
            <div class="absolute inset-0 bg-gradient-to-r from-amber-200/20 to-yellow-500/20 rounded-full blur-sm animate-pulse scale-110"></div>
            <div class="absolute inset-0 border-2 border-amber-200/30 rounded-full animate-spin-slow"></div>
            
            <!-- Main image -->
            <img class="relative z-10 w-72 h-72 md:w-80 md:h-80 rounded-full mb-3 fadein-up object-cover border-4 border-amber-200/50 shadow-2xl group-hover:scale-105 transition-all duration-300"
            :src="require('@/assets/img/profil.jpg')" alt="Profile Photo">
            
            <!-- Floating particles -->
            <div class="absolute top-8 right-8 w-3 h-3 bg-amber-400 rounded-full animate-bounce opacity-75"></div>
            <div class="absolute bottom-12 left-12 w-2 h-2 bg-yellow-500 rounded-full animate-bounce delay-300 opacity-60"></div>
            <div class="absolute top-1/2 right-4 w-1.5 h-1.5 bg-amber-300 rounded-full animate-pulse delay-500"></div>
          </div>
        </div>
        
        <!-- Text Content -->
        <div class="md:w-7/12 lg:w-8/12 space-y-6">
          <div class="relative">
            <p class="mb-6 fadein-left fadeins-1 leading-relaxed text-gray-300 relative z-10 p-6 bg-gradient-to-r from-[#2a2a2b]/50 to-transparent rounded-2xl border border-amber-200/10 backdrop-blur-sm">
              <span class="text-4xl text-amber-200 font-serif absolute -top-2 -left-2">"</span>
              &nbsp; &nbsp; &nbsp; Hi everyone! My name is <span class="text-amber-200 font-semibold">Tegar Mallisa</span>. I'm a web developer from Sleman, Special Region of Yogyakarta. I
              Experienced in building user interface using Nuxt JS framework. Understand UI/UX principles, API integration, and database management. Accustomed to working independently and in teams, and ready to contribute in creating functional and attractive digital solutions.
              <span class="text-4xl text-amber-200 font-serif absolute -bottom-6 -right-2">"</span>
            </p>
          </div>
          
          <div class="relative">
            <p class="mb-6 fadein-left fadeins-2 leading-relaxed text-gray-300 p-6 bg-gradient-to-l from-[#2a2a2b]/50 to-transparent rounded-2xl border border-amber-200/10 backdrop-blur-sm">
              &nbsp; &nbsp; &nbsp; I have experience as a <span class="text-yellow-400 font-semibold">Frontend Web Developer</span> at PT. Gama Integra Informatika, focusing on building user interfaces with Nuxt JS, API integration, and version control for team collaboration. 
              Previously, I also interned as an <span class="text-yellow-400 font-semibold">SEO Specialist</span> at CV. Rumah Mesin, where I was responsible for creating SEO-friendly content, and conducting keyword research.
            </p>
          </div>


        </div>
      </section>
    </article>
  </div>

  <!-- Skills Section -->
  <div class="relative px-6 py-8 md:px-12 md:py-12 text-left text-amber-50 mx-3 overflow-hidden">
    
    <!-- Background decorative elements -->
    <div class="absolute inset-0 overflow-hidden pointer-events-none">
      <div class="absolute top-1/4 left-10 w-64 h-64 bg-gradient-to-r from-amber-200/3 to-yellow-500/3 rounded-full blur-3xl animate-float-slow"></div>
      <div class="absolute bottom-1/4 right-10 w-48 h-48 bg-gradient-to-l from-amber-300/3 to-orange-500/3 rounded-full blur-2xl animate-float-delay"></div>
    </div>

    <article data-page="skills" class="relative z-10">
      <header>
        <div class="text-3xl font-bold text-white mb-8 fadein-bot title-section flex items-center">
          <div class="h-[2px] w-20 md:w-32 bg-gradient-to-r from-transparent via-amber-200 to-yellow-500 rounded-full aos-init aos-animate mr-4" 
               data-aos="zoom-in-right" data-aos-duration="600"></div>
          <span class="bg-gradient-to-r from-amber-200 to-yellow-500 bg-clip-text text-transparent">Skills</span>
        </div>
      </header>
      
      <section>
        <!-- Enhanced Tab Navigation -->
        <div class="mb-8">
          <ul class="flex flex-wrap text-sm font-medium text-center mb-6">
            <li class="mr-3">
              <button 
                class="relative inline-block px-6 py-3 rounded-2xl transition-all duration-300 font-semibold overflow-hidden group"
                :class="{ 
                  'text-amber-900 bg-gradient-to-r from-amber-200 to-yellow-500 shadow-lg transform scale-105': activeTab === 1,
                  'text-gray-400 hover:text-amber-200 border border-amber-200/30 hover:border-amber-200/60': activeTab !== 1
                }" 
                @click="activeTab = 1">
                <span class="relative z-10">🚀 Tech Stack</span>
                <div v-if="activeTab !== 1" class="absolute inset-0 bg-gradient-to-r from-amber-200/0 to-yellow-500/0 group-hover:from-amber-200/10 group-hover:to-yellow-500/10 transition-all duration-300"></div>
              </button>
            </li>
            <li class="mr-3">
              <button 
                class="relative inline-block px-6 py-3 rounded-2xl transition-all duration-300 font-semibold overflow-hidden group"
                :class="{ 
                  'text-amber-900 bg-gradient-to-r from-amber-200 to-yellow-500 shadow-lg transform scale-105': activeTab === 2,
                  'text-gray-400 hover:text-amber-200 border border-amber-200/30 hover:border-amber-200/60': activeTab !== 2
                }" 
                @click="activeTab = 2">
                <span class="relative z-10">🛠️ Tools</span>
                <div v-if="activeTab !== 2" class="absolute inset-0 bg-gradient-to-r from-amber-200/0 to-yellow-500/0 group-hover:from-amber-200/10 group-hover:to-yellow-500/10 transition-all duration-300"></div>
              </button>
            </li>
          </ul>
        </div>

        <!-- Tech Stack Tab -->
        <div v-show="activeTab === 1" class="animate-fade-in">
          <div class="grid grid-cols-1 gap-6 pb-20 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4">
            <div v-for="(item, index) in tech" :key="item.id" 
                 class="skill-card group"
                 :style="{ animationDelay: `${index * 100}ms` }">
              <div class="relative overflow-hidden rounded-2xl border border-amber-200/20 bg-gradient-to-br from-[#2a2a2b]/80 to-[#1e1e1f]/80 backdrop-blur-sm p-6 transition-all duration-500 hover:border-amber-200/60 hover:shadow-2xl hover:shadow-amber-200/10 hover:-translate-y-2">
                
                <!-- Background glow effect -->
                <div class="absolute inset-0 bg-gradient-to-r from-amber-500/0 via-yellow-500/0 to-amber-500/0 group-hover:from-amber-500/5 group-hover:via-yellow-500/10 group-hover:to-amber-500/5 transition-all duration-500 rounded-2xl"></div>
                
                <!-- Content -->
                <div class="relative z-10">
                  <!-- Icon -->
                  <div class="flex justify-center mb-4">
                    <div class="relative p-3 rounded-2xl bg-gradient-to-br from-amber-200/10 to-yellow-500/5 group-hover:from-amber-200/20 group-hover:to-yellow-500/10 transition-all duration-300">
                      <img 
                        alt="item.name" 
                        loading="lazy" 
                        width="48" 
                        height="48" 
                        decoding="async" 
                        class="w-12 h-12 object-contain drop-shadow-lg transition-all duration-300 group-hover:scale-110 group-hover:rotate-6"
                        :src="item.imageUrl">
                    </div>
                  </div>
                  
                  <!-- Name -->
                  <h3 class="text-lg font-bold text-center mb-2 text-white group-hover:text-amber-200 transition-colors duration-300">
                    {{ item.name }}
                  </h3>
                  
                  <!-- Status -->
                  <p class="text-center text-sm font-medium transition-colors duration-300"
                     :class="getStatusColor(item.status)">
                    {{ item.status }}
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>

        <!-- Tools Tab -->
        <div v-show="activeTab === 2" class="animate-fade-in">
          <div class="grid grid-cols-1 gap-6 pb-20 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4">
            <div v-for="(item, index) in tools" :key="item.id" 
                 class="skill-card group"
                 :style="{ animationDelay: `${index * 100}ms` }">
              <div class="relative overflow-hidden rounded-2xl border border-amber-200/20 bg-gradient-to-br from-[#2a2a2b]/80 to-[#1e1e1f]/80 backdrop-blur-sm p-6 transition-all duration-500 hover:border-amber-200/60 hover:shadow-2xl hover:shadow-amber-200/10 hover:-translate-y-2">
                
                <!-- Background glow effect -->
                <div class="absolute inset-0 bg-gradient-to-r from-amber-500/0 via-yellow-500/0 to-amber-500/0 group-hover:from-amber-500/5 group-hover:via-yellow-500/10 group-hover:to-amber-500/5 transition-all duration-500 rounded-2xl"></div>
                
                <!-- Content -->
                <div class="relative z-10">
                  <!-- Icon -->
                  <div class="flex justify-center mb-4">
                    <div class="relative p-3 rounded-2xl bg-gradient-to-br from-amber-200/10 to-yellow-500/5 group-hover:from-amber-200/20 group-hover:to-yellow-500/10 transition-all duration-300">
                      <img 
                        alt="item.name" 
                        loading="lazy" 
                        width="48" 
                        height="48" 
                        decoding="async" 
                        class="w-12 h-12 object-contain drop-shadow-lg transition-all duration-300 group-hover:scale-110 group-hover:rotate-6"
                        :src="item.imageUrl">
                    </div>
                  </div>
                  
                  <!-- Name -->
                  <h3 class="text-lg font-bold text-center mb-2 text-white group-hover:text-amber-200 transition-colors duration-300">
                    {{ item.name }}
                  </h3>
                  
                  <!-- Status -->
                  <p class="text-center text-sm font-medium transition-colors duration-300"
                     :class="getStatusColor(item.status)">
                    {{ item.status }}
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </article>
  </div>
</template>

<style>
/* Enhanced animations */
.fadein-left {
  opacity: 0;
  animation: fadeInLeft 0.8s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards;
}

@keyframes fadeInLeft {
  0% {
    opacity: 0;
    transform: translateX(-30px);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

.fadeins-1 { animation-delay: 500ms; }
.fadeins-2 { animation-delay: 800ms; }
.fadeins-3 { animation-delay: 1100ms; }

.fadein-bot {
  opacity: 0;
  animation: fadeInBot 0.8s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards;
  animation-delay: 300ms;
}

@keyframes fadeInBot {
  from {
    opacity: 0;
    transform: translate3d(0, 30px, 0) scale(0.95);
  }
  to {
    opacity: 1;
    transform: translate3d(0, 0, 0) scale(1);
  }
}

.fadein-up {
  opacity: 0;
  animation: fadeInUp 0.8s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards;
  animation-delay: 400ms;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translate3d(0, 30px, 0) scale(0.9);
  }
  to {
    opacity: 1;
    transform: translate3d(0, 0, 0) scale(1);
  }
}

/* Skill card animations */
.skill-card {
  opacity: 0;
  animation: slideInUp 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards;
}

@keyframes slideInUp {
  from {
    opacity: 0;
    transform: translateY(40px) scale(0.95);
  }
  to {
    opacity: 1;
    transform: translateY(0) scale(1);
  }
}

/* Tab content fade animation */
.animate-fade-in {
  animation: fadeIn 0.5s ease-in-out;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

/* Floating animations */
.animate-float {
  animation: float 6s ease-in-out infinite;
}

.animate-float-delay {
  animation: float 6s ease-in-out infinite;
  animation-delay: -3s;
}

.animate-float-slow {
  animation: floatSlow 8s ease-in-out infinite;
}

@keyframes float {
  0%, 100% { transform: translateY(0px) rotate(0deg); }
  50% { transform: translateY(-20px) rotate(5deg); }
}

@keyframes floatSlow {
  0%, 100% { transform: translateY(0px) translateX(0px); }
  25% { transform: translateY(-10px) translateX(10px); }
  75% { transform: translateY(10px) translateX(-10px); }
}

/* Spin animation for decorative elements */
.animate-spin-slow {
  animation: spin 20s linear infinite;
}

@keyframes spin {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}

/* Enhanced hover effects */
.skill-card:hover {
  transform: translateY(-8px) scale(1.02);
}

/* Custom scrollbar for better aesthetics */
::-webkit-scrollbar {
  width: 8px;
}

::-webkit-scrollbar-track {
  background: rgba(0, 0, 0, 0.1);
  border-radius: 4px;
}

::-webkit-scrollbar-thumb {
  background: linear-gradient(45deg, #fbbf24, #f59e0b);
  border-radius: 4px;
}

::-webkit-scrollbar-thumb:hover {
  background: linear-gradient(45deg, #f59e0b, #d97706);
}

/* Responsive improvements */
@media (max-width: 768px) {
  .skill-card {
    margin-bottom: 1rem;
  }
}
</style>