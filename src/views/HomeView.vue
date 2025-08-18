<template>
  <main
    class="mt-10 md:mt-1 flex flex-col-reverse gap-8 items-center md:flex-row md:gap-16 md:justify-center min-h-[65vh] md:min-h-[80vh] relative overflow-hidden">
    
    <!-- Background decorative elements -->
    <div class="absolute inset-0 overflow-hidden pointer-events-none">
      <div class="absolute top-20 left-10 w-32 h-32 bg-amber-200/10 rounded-full blur-xl animate-float"></div>
      <div class="absolute bottom-20 right-10 w-40 h-40 bg-yellow-500/10 rounded-full blur-xl animate-float-delay"></div>
      <div class="absolute top-1/2 left-1/4 w-24 h-24 bg-amber-300/5 rounded-full blur-lg animate-pulse"></div>
    </div>

    <div class="space-y-4 text-center md:text-left px-10 relative z-10">
      <!-- Greeting with enhanced styling -->
      <div class="relative">
        <p class="text-amber-200 text-lg font-medium tracking-wide fadein-up">Hello World, I'm</p>
        <div class="absolute -top-2 -left-2 w-2 h-2 bg-amber-400 rounded-full animate-ping opacity-75"></div>
      </div>
      
      <!-- Main name with gradient and shadow -->
      <h1 class="text-4xl font-bold md:text-6xl text-transparent bg-clip-text bg-gradient-to-r from-white via-amber-100 to-amber-300 fadein-up drop-shadow-lg leading-tight py-2">
        Tegar Mallisa
      </h1>
      
      <!-- Typewriter section with enhanced background -->
      <div class="py-4 relative">
        <div class="absolute inset-0 bg-gradient-to-r from-transparent via-amber-500/5 to-transparent rounded-lg blur-sm"></div>
        <h1
          class="typewrite text-xl font-semibold text-transparent bg-clip-text bg-gradient-to-r from-slate-100 via-amber-200 to-yellow-500 md:text-3xl fadein-up relative z-10"
          ref="typewriter">
          <span class="wrap">{{ txt }}</span>
        </h1>
      </div>
      
      <!-- Welcome message with enhanced styling -->
      <div class="fade-in-from-left">
        <p class="text-white/90 text-lg pr-4 font-light">
          Welcome to My personal website. 
          <span class="wave inline-block ml-2">👋🏼</span>
        </p>
        <div class="w-24 h-1 bg-gradient-to-r from-amber-400 to-yellow-500 rounded-full mt-2 mx-auto md:mx-0"></div>
      </div>

      <!-- Enhanced Download Resume Button -->
      <div class="pt-6 fadein-bot fade-500">
        <button
          @click="downloadResume"
          class="group relative flex items-center py-3 px-6 mx-auto md:mx-0 text-sm font-semibold rounded-xl border-2 transition-all duration-300 transform hover:scale-105 text-amber-200 border-amber-200 hover:bg-amber-200 hover:text-gray-900 bg-transparent focus:outline-none focus:ring-4 focus:ring-amber-200/30 w-fit shadow-lg hover:shadow-amber-200/25 hover:shadow-xl">
          
          <!-- Animated background -->
          <div class="absolute inset-0 bg-gradient-to-r from-amber-400/0 via-amber-400/0 to-amber-400/0 group-hover:from-amber-400/10 group-hover:via-amber-400/20 group-hover:to-amber-400/10 rounded-xl transition-all duration-300"></div>
          
          <!-- Download icon with animation -->
          <svg
            xmlns="http://www.w3.org/2000/svg" 
            viewBox="0 0 24 24" 
            fill="currentColor" 
            class="mr-3 w-5 h-5 transform group-hover:translate-y-0.5 transition-transform duration-200">
            <path fill-rule="evenodd"
              d="M5.625 1.5H9a3.75 3.75 0 013.75 3.75v1.875c0 1.036.84 1.875 1.875 1.875H16.5a3.75 3.75 0 013.75 3.75v7.875c0 1.035-.84 1.875-1.875 1.875H5.625a1.875 1.875 0 01-1.875-1.875V3.375c0-1.036.84-1.875 1.875-1.875zm5.845 17.03a.75.75 0 001.06 0l3-3a.75.75 0 10-1.06-1.06l-1.72 1.72V12a.75.75 0 00-1.5 0v4.19l-1.72-1.72a.75.75 0 00-1.06 1.06l3 3z"
              clip-rule="evenodd"></path>
            <path
              d="M14.25 5.25a5.23 5.23 0 00-1.279-3.434 9.768 9.768 0 016.963 6.963A5.23 5.23 0 0016.5 7.5h-1.875a.375.375 0 01-.375-.375V5.25z">
            </path>
          </svg>
          
          <!-- Button text -->
          <span class="relative z-10">Download Resume</span>
          
          <!-- Shine effect -->
          <div class="absolute inset-0 rounded-xl opacity-0 group-hover:opacity-100 transition-opacity duration-300">
            <div class="absolute inset-0 bg-gradient-to-r from-transparent via-white/10 to-transparent skew-x-12 -translate-x-full group-hover:translate-x-full transition-transform duration-700"></div>
          </div>
        </button>
      </div>
    </div>

    <!-- Enhanced profile image section -->
    <div class="flex justify-center md:justify-start fadein-right relative">
      <!-- Decorative rings -->
      <div class="absolute inset-0 rounded-full border border-amber-200/20 animate-ping-slow scale-110"></div>
      <div class="absolute inset-0 rounded-full border border-yellow-500/30 animate-pulse scale-125"></div>
      
      <!-- Main image container -->
      <div class="relative group">
        <img 
  alt="avatar" 
  fetchpriority="high" 
  width="300" 
  height="300" 
  decoding="async" 
  data-nimg="1"
  class="w-10/12 md:h-auto rounded-full border-4 border-amber-200 pict relative z-10 transition-all duration-300 group-hover:scale-105 group-hover:rotate-2"
  :src="require('@/img/profil.jpg')">
        
        <!-- Floating particles effect -->
        <div class="absolute top-4 right-4 w-2 h-2 bg-amber-400 rounded-full animate-bounce opacity-75"></div>
        <div class="absolute bottom-6 left-6 w-1.5 h-1.5 bg-yellow-500 rounded-full animate-bounce delay-300 opacity-60"></div>
        <div class="absolute top-1/2 -right-2 w-1 h-1 bg-amber-300 rounded-full animate-pulse"></div>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: 'HomeView',
  data() {
    return {
      toRotate: ["Web Developer", "Information Systems", "Frontend Web Developer"],
      period: 2000,
      txt: '',
      loopNum: 0,
      isDeleting: false,
      // Ganti URL ini dengan link Google Drive Anda yang berisi file PDF resume
      resumeUrl: 'https://drive.google.com/file/d/YOUR_FILE_ID/view?usp=sharing'
    };
  },
  mounted() {
    this.$nextTick(() => {
      this.tick();
    });
  },
  methods: {
    tick() {
      let typewriter = this.$refs.typewriter;

      if (!typewriter) {
        return;
      }

      let i = this.loopNum % this.toRotate.length;
      let fullTxt = this.toRotate[i];

      this.txt = this.isDeleting ? fullTxt.substring(0, this.txt.length - 1) : fullTxt.substring(0, this.txt.length + 1);
      typewriter.innerHTML = `<span class="wrap">${this.txt}</span>`;

      let that = this;
      let delta = 200 - Math.random() * 100;

      if (this.isDeleting) {
        delta /= 2;
      }

      if (!this.isDeleting && this.txt === fullTxt) {
        delta = this.period;
        this.isDeleting = true;
      } else if (this.isDeleting && this.txt === '') {
        this.isDeleting = false;
        this.loopNum++;
        delta = 500;
      }

      setTimeout(() => {
        that.tick();
      }, delta);
    },
    
    downloadResume() {
      // Membuka link Google Drive di tab baru
      window.open(this.resumeUrl, '_blank');
    }
  }
}
</script>

<style>
body {
  overflow-y: scroll;
  overflow-x: hidden;
}

.typewrite > .wrap {
  border-right: 0.08em solid #fff;
  animation: blink 1s infinite;
}

@keyframes blink {
  0%, 50% { border-color: #fff; }
  51%, 100% { border-color: transparent; }
}

.wave {
  animation-name: wave-animation;
  animation-duration: 2.5s;
  animation-iteration-count: infinite;
  transform-origin: 70% 70%;
  display: inline-block;
}

@keyframes wave-animation {
  0% { transform: rotate(0deg) }
  10% { transform: rotate(14deg) }
  20% { transform: rotate(-8deg) }
  30% { transform: rotate(14deg) }
  40% { transform: rotate(-4deg) }
  50% { transform: rotate(10deg) }
  60% { transform: rotate(0deg) }
  to { transform: rotate(0deg) }
}

.pict {
  box-shadow: 
    0px 0px 73px -9px rgba(255,219,112,0.44),
    0px 0px 40px -5px rgba(255,193,7,0.2),
    inset 0px 0px 20px rgba(255,219,112,0.1);
  -webkit-box-shadow: 
    0px 0px 73px -9px rgba(255,219,112,0.44),
    0px 0px 40px -5px rgba(255,193,7,0.2),
    inset 0px 0px 20px rgba(255,219,112,0.1);
  -moz-box-shadow: 
    0px 0px 73px -9px rgba(255,219,112,0.44),
    0px 0px 40px -5px rgba(255,193,7,0.2),
    inset 0px 0px 20px rgba(255,219,112,0.1);
}

/* Enhanced animations */
.fadein-up {
  opacity: 0;
  animation-name: fadeInUp;
  animation-duration: 0.8s;
  animation-fill-mode: forwards;
  animation-delay: 500ms;
  animation-timing-function: cubic-bezier(0.175, 0.885, 0.32, 1.275);
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translate3d(0, 50px, 0);
  }
  to {
    opacity: 1;
    transform: translate3d(0, 0, 0);
  }
}

.fade-in-from-left {
  opacity: 0;
  animation: fadeInLeft 0.8s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards;
  animation-delay: 700ms;
}

@keyframes fadeInLeft {
  0% {
    opacity: 0;
    transform: translateX(-50px);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

.fadein-right {
  opacity: 0;
  animation: fadeInRight 0.8s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards;
  animation-delay: 600ms;
}

@keyframes fadeInRight {
  0% {
    opacity: 0;
    transform: translateX(50px) scale(0.9);
  }
  100% {
    opacity: 1;
    transform: translateX(0) scale(1);
  }
}

.fadein-bot {
  opacity: 0;
  animation: fadeInBot 0.8s cubic-bezier(0.175, 0.885, 0.32, 1.275) forwards;
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

/* New floating animations */
.animate-float {
  animation: float 6s ease-in-out infinite;
}

.animate-float-delay {
  animation: float 6s ease-in-out infinite;
  animation-delay: -3s;
}

@keyframes float {
  0%, 100% {
    transform: translateY(0px) rotate(0deg);
  }
  50% {
    transform: translateY(-20px) rotate(10deg);
  }
}

.animate-ping-slow {
  animation: ping-slow 4s cubic-bezier(0, 0, 0.2, 1) infinite;
}

@keyframes ping-slow {
  0% {
    transform: scale(1);
    opacity: 1;
  }
  75%, 100% {
    transform: scale(1.1);
    opacity: 0;
  }
}

/* Delay classes */
.fadein-1 { animation-delay: 200ms; }
.fadein-2 { animation-delay: 400ms; }
.fadein-3 { animation-delay: 600ms; }
.fade-500 { animation-delay: 900ms; }

/* Responsive enhancements */
@media (max-width: 768px) {
  .pict {
    width: 280px;
    height: 280px;
  }
}

/* Smooth scrolling */
html {
  scroll-behavior: smooth;
}

/* Custom scrollbar */
::-webkit-scrollbar {
  width: 8px;
}

::-webkit-scrollbar-track {
  background: rgba(0, 0, 0, 0.1);
}

::-webkit-scrollbar-thumb {
  background: rgba(251, 191, 36, 0.5);
  border-radius: 4px;
}

::-webkit-scrollbar-thumb:hover {
  background: rgba(251, 191, 36, 0.7);
}
</style>