<template>
  <div class="container mx-auto p-3 md:p-8 min-h-screen relative overflow-hidden">
    <!-- Background decorative elements -->
    <div class="absolute inset-0 overflow-hidden pointer-events-none">
      <div class="floating-shape shape-1"></div>
      <div class="floating-shape shape-2"></div>
      <div class="floating-shape shape-3"></div>
      <div class="floating-shape shape-4"></div>
    </div>
    
    <div class="max-w-4xl mx-auto relative z-10">
      <div class="flex flex-col gap-6 fade-zoom-up">
        <!-- Header Section -->
        <div class="text-center mb-8 pt-4">
          <div class="inline-block mb-6">
            <div class="pulse-ring"></div>
            <div class="pulse-ring pulse-ring-delay"></div>
            <h1 class="text-4xl md:text-5xl font-bold bg-clip-text bg-gradient-to-r from-slate-100 via-amber-300 to-orange-400 text-transparent mb-6 animate-text-shine leading-tight">
              Contact Me
            </h1>
          </div>
          <p class="text-slate-400 text-lg max-w-2xl mx-auto leading-relaxed">
            Feel free to contact me. I am open to discussing job opportunities and further recruitment processes.
          </p>
          
          <!-- Decorative line -->
          <div class="flex items-center justify-center mt-6">
            <div class="h-px bg-gradient-to-r from-transparent via-amber-400 to-transparent w-32"></div>
            <div class="mx-4">
              <div class="w-2 h-2 bg-amber-400 rounded-full animate-pulse"></div>
            </div>
            <div class="h-px bg-gradient-to-r from-transparent via-amber-400 to-transparent w-32"></div>
          </div>
        </div>

        <!-- Contact Cards -->
        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 md:gap-6">
          <!-- Email -->
          <div class="contact-card group" @click="openEmail()">
            <div class="card-glow"></div>
            <div class="flex items-center relative z-10">
              <div class="contact-icon bg-gradient-to-br from-blue-600 to-blue-800 group-hover:from-blue-500 group-hover:to-blue-700 group-hover:scale-110">
                <svg class="w-6 h-6 group-hover:animate-bounce" fill="currentColor" viewBox="0 0 20 20">
                  <path d="M2.003 5.884L10 9.882l7.997-3.998A2 2 0 0016 4H4a2 2 0 00-1.997 1.884z"></path>
                  <path d="M18 8.118l-8 4-8-4V14a2 2 0 002 2h12a2 2 0 002-2V8.118z"></path>
                </svg>
              </div>
              <div class="ml-4 flex-1">
                <h3 class="text-amber-200 font-semibold text-lg group-hover:text-amber-100 transition-colors">Email</h3>
                <p class="text-slate-400 text-sm mb-2 group-hover:text-slate-300 transition-colors">Kirim email untuk diskusi atau kerjasama</p>
                <div class="items-center">
                  <span class="text-white group-hover:text-amber-200 transition-colors font-medium">
                    tegarmallisa27@gmail.com
                  </span>
                </div>
              </div>
            </div>
          </div>

          <!-- WhatsApp -->
          <div class="contact-card group" @click="openWhatsApp()">
            <div class="card-glow"></div>
            <div class="flex items-center relative z-10">
              <div class="contact-icon bg-gradient-to-br from-green-600 to-green-800 group-hover:from-green-500 group-hover:to-green-700 group-hover:scale-110">
                <svg class="w-6 h-6 group-hover:animate-bounce" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893A11.821 11.821 0 0020.885 3.488"/>
                </svg>
              </div>
              <div class="ml-4 flex-1">
                <h3 class="text-amber-200 font-semibold text-lg group-hover:text-amber-100 transition-colors">WhatsApp</h3>
                <p class="text-slate-400 text-sm mb-2 group-hover:text-slate-300 transition-colors">Chat langsung untuk respon cepat</p>
                <div class="items-center">
                  <span class="text-white group-hover:text-amber-200 transition-colors font-medium">
                    +62 815-4005-2395
                  </span>
                </div>
              </div>
            </div>
          </div>

          <!-- LinkedIn -->
          <div class="contact-card group" @click="openLink('https://www.linkedin.com/in/tegarmallisa')">
            <div class="card-glow"></div>
            <div class="flex items-center relative z-10">
              <div class="contact-icon bg-gradient-to-br from-blue-700 to-blue-900 group-hover:from-blue-600 group-hover:to-blue-800 group-hover:scale-110">
                <svg class="w-6 h-6 group-hover:animate-bounce" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
                </svg>
              </div>
              <div class="ml-4 flex-1">
                <h3 class="text-amber-200 font-semibold text-lg group-hover:text-amber-100 transition-colors">LinkedIn</h3>
                <p class="text-slate-400 text-sm mb-2 group-hover:text-slate-300 transition-colors">Terhubung untuk peluang profesional</p>
                <div class="items-center">
                  <span class="text-white group-hover:text-amber-200 transition-colors font-medium">
                    linkedin.com/in/tegarmallisa
                  </span>
                </div>
              </div>
            </div>
          </div>

          <!-- Instagram -->
          <div class="contact-card group" @click="openLink('https://instagram.com/garmalls')">
            <div class="card-glow"></div>
            <div class="flex items-center relative z-10">
              <div class="contact-icon bg-gradient-to-br from-purple-600 via-pink-600 to-orange-500 group-hover:from-purple-500 group-hover:via-pink-500 group-hover:to-orange-400 group-hover:scale-110">
                <svg class="w-6 h-6 group-hover:animate-bounce" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
                </svg>
              </div>
              <div class="ml-4 flex-1">
                <h3 class="text-amber-200 font-semibold text-lg group-hover:text-amber-100 transition-colors">Instagram</h3>
                <p class="text-slate-400 text-sm mb-2 group-hover:text-slate-300 transition-colors">Ikuti untuk update dan konten visual</p>
                <div class="items-center">
                  <span class="text-white group-hover:text-amber-200 transition-colors font-medium">
                    @garmalls
                  </span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Toast Notification -->
    <transition name="toast">
      <div v-if="showToast" class="fixed top-6 right-6 z-50 max-w-sm">
        <div class="bg-green-600 text-white px-6 py-4 rounded-lg shadow-lg flex items-center">
          <svg class="w-6 h-6 mr-3 flex-shrink-0" fill="currentColor" viewBox="0 0 20 20">
            <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zm3.707-9.293a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z" clip-rule="evenodd"></path>
          </svg>
          <div>
            <p class="font-semibold">{{ toastMessage.title }}</p>
            <p class="text-sm opacity-90">{{ toastMessage.description }}</p>
          </div>
        </div>
      </div>
    </transition>
  </div>
</template>
  
<script>
export default {
  data() {
    return {
      showToast: false,
      toastMessage: {
        title: '',
        description: ''
      }
    }
  },
  methods: {
    showToastMessage(title, description) {
      this.toastMessage = { title, description };
      this.showToast = true;
      setTimeout(() => {
        this.showToast = false;
      }, 4000);
    },
    
    openEmail() {
      const email = 'tegarmallisa27@gmail.com';
      const subject = 'Inquiry from Portfolio Website';
      const body = 'Hello,\n\nI would like to get in touch with you regarding...';
      
      // Gmail compose URL
      const gmailUrl = `https://mail.google.com/mail/?view=cm&fs=1&to=${encodeURIComponent(email)}&su=${encodeURIComponent(subject)}&body=${encodeURIComponent(body)}`;
      
      window.open(gmailUrl, '_blank');
    },
    
    openWhatsApp() {
      window.open('https://wa.me/6281540052395', '_blank');
    },
    
    openLink(url) {
      window.open(url, '_blank');
    }
  }
}
</script>

<style scoped>
/* Background decorative elements */
.floating-shape {
  position: absolute;
  border-radius: 50%;
  opacity: 0.1;
  animation: float 6s ease-in-out infinite;
}

.shape-1 {
  width: 100px;
  height: 100px;
  background: linear-gradient(45deg, #f59e0b, #f97316);
  top: 10%;
  left: 10%;
  animation-delay: 0s;
}

.shape-2 {
  width: 60px;
  height: 60px;
  background: linear-gradient(45deg, #3b82f6, #1d4ed8);
  top: 60%;
  right: 15%;
  animation-delay: 2s;
}

.shape-3 {
  width: 80px;
  height: 80px;
  background: linear-gradient(45deg, #10b981, #059669);
  bottom: 20%;
  left: 20%;
  animation-delay: 4s;
}

.shape-4 {
  width: 40px;
  height: 40px;
  background: linear-gradient(45deg, #8b5cf6, #7c3aed);
  top: 30%;
  right: 30%;
  animation-delay: 1s;
}

@keyframes float {
  0%, 100% { transform: translateY(0px) rotate(0deg); }
  50% { transform: translateY(-20px) rotate(180deg); }
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
  animation: pulse 2s infinite;
}

.pulse-ring-delay {
  animation-delay: 1s;
  border-color: rgba(245, 158, 11, 0.2);
}

@keyframes pulse {
  0% {
    transform: translate(-50%, -50%) scale(0.8);
    opacity: 1;
  }
  100% {
    transform: translate(-50%, -50%) scale(1.2);
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
  animation: text-shine 3s ease-in-out infinite;
}

/* Contact cards */
.contact-card {
  @apply bg-[#1e1e1f] border border-[#383838] rounded-xl p-5 md:p-6 hover:bg-[#282828] transition-all duration-500 cursor-pointer relative overflow-hidden;
  transform: translateY(0);
}

.contact-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.3), 0 10px 10px -5px rgba(0, 0, 0, 0.1);
}

.card-glow {
  position: absolute;
  inset: 0;
  background: linear-gradient(45deg, rgba(245, 158, 11, 0.1), rgba(249, 115, 22, 0.1));
  opacity: 0;
  transition: opacity 0.5s ease;
  border-radius: inherit;
}

.contact-card:hover .card-glow {
  opacity: 1;
}

.contact-icon {
  @apply w-14 h-14 rounded-full flex items-center justify-center text-white transition-all duration-300 shadow-lg;
}

/* Toast animations */
.toast-enter-active, .toast-leave-active {
  transition: all 0.5s ease;
}

.toast-enter-from {
  opacity: 0;
  transform: translateX(100%) scale(0.8);
}

.toast-leave-to {
  opacity: 0;
  transform: translateX(100%) scale(0.8);
}

/* Main animation */
@keyframes fadeZoomUp {
  0% {
    opacity: 0;
    transform: scale(0.8) translateY(30px);
  }
  100% {
    opacity: 1;
    transform: scale(1) translateY(0);
  }
}

.fade-zoom-up {
  animation: fadeZoomUp 1.2s cubic-bezier(0.25, 0.46, 0.45, 0.94);
}

/* Responsive improvements */
@media (max-width: 768px) {
  .contact-card {
    @apply p-4;
  }
  
  .contact-icon {
    @apply w-12 h-12;
  }
  
  .floating-shape {
    opacity: 0.05;
  }
  
  .pulse-ring {
    width: 200px;
    height: 200px;
  }
}
</style>