<template>
  <header class="sticky top-0 z-30 bg-white/95 backdrop-blur border-b border-slate-200">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-16 lg:h-20">
        <!-- Logo -->
        <a href="/" class="flex items-center gap-2 text-bluice-800 font-extrabold text-xl tracking-tight">
          <span class="w-8 h-8 rounded-lg bg-bluice-800 flex items-center justify-center text-white text-sm font-bold">Prof</span>
          Mu Gomes
        </a>

        <!-- Nav desktop -->
        <nav class="hidden md:flex items-center gap-8 text-sm font-medium text-slate-600">
          <a href="#sobre" class="hover:text-bluice-700 transition-colors">Sobre</a>
          <a href="#projetos" class="hover:text-bluice-700 transition-colors">Projetos</a>
          <a href="#assinantes" class="hover:text-bluice-700 transition-colors">Assinantes</a>
          <a href="#loja" class="hover:text-bluice-700 transition-colors">Loja</a>
          <a href="#contato" class="hover:text-bluice-700 transition-colors">Contato</a>
        </nav>

        <!-- CTA desktop -->
        <div class="hidden md:flex items-center gap-3">
          <a href="https://github.com/profmugomes" target="_blank" rel="noopener noreferrer" class="text-sm font-medium text-slate-600 hover:text-bluice-700 transition-colors px-4 py-2">
            GitHub
          </a>
          <a href="https://youtube.com/@profmugomes" target="_blank" rel="noopener noreferrer" class="text-sm font-semibold text-white bg-emerald-600 hover:bg-emerald-700 transition-colors px-5 py-2.5 rounded-lg shadow-sm">
            YouTube
          </a>
        </div>

        <!-- Mobile hamburger -->
        <button class="md:hidden p-2 rounded-lg hover:bg-slate-100 text-slate-600" @click="openDrawer">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/>
          </svg>
        </button>
      </div>
    </div>

    <!-- Overlay -->
    <div
      v-show="drawerOpen"
      class="fixed inset-0 z-40 bg-black/50 md:hidden transition-opacity duration-300"
      @click="closeDrawer"
    ></div>

    <!-- Drawer (sidebar) -->
    <aside
      class="fixed top-0 left-0 z-50 w-72 h-screen bg-bluice-900 shadow-2xl md:hidden transform transition-transform duration-300 ease-in-out overflow-y-auto"
      :class="drawerOpen ? 'translate-x-0' : '-translate-x-full'"
    >
      <!-- Drawer header -->
      <div class="flex items-center justify-between px-5 py-5 border-b border-bluice-700">
        <a href="/" class="flex items-center gap-2 text-white font-extrabold text-lg" @click="closeDrawer">
          <span class="w-8 h-8 rounded-lg bg-white/20 flex items-center justify-center text-white text-sm font-bold">Prof</span>
          Mu Gomes
        </a>
        <button class="p-1.5 rounded-lg text-bluice-300 hover:bg-bluice-800 hover:text-white transition-colors" @click="closeDrawer">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"/>
          </svg>
        </button>
      </div>

      <!-- Drawer nav -->
      <nav class="p-4 space-y-1">
        <a href="#sobre" class="flex items-center gap-3 px-4 py-3 rounded-lg text-sm font-medium text-bluice-100 hover:bg-bluice-800 hover:text-white transition-colors" @click="closeDrawer">
          <span class="text-lg">👤</span> Sobre
        </a>
        <a href="#projetos" class="flex items-center gap-3 px-4 py-3 rounded-lg text-sm font-medium text-bluice-100 hover:bg-bluice-800 hover:text-white transition-colors" @click="closeDrawer">
          <span class="text-lg">📦</span> Projetos
        </a>
        <a href="#assinantes" class="flex items-center gap-3 px-4 py-3 rounded-lg text-sm font-medium text-bluice-100 hover:bg-bluice-800 hover:text-white transition-colors" @click="closeDrawer">
          <span class="text-lg">🎫</span> Assinantes
        </a>
        <a href="#loja" class="flex items-center gap-3 px-4 py-3 rounded-lg text-sm font-medium text-bluice-100 hover:bg-bluice-800 hover:text-white transition-colors" @click="closeDrawer">
          <span class="text-lg">🛒</span> Loja
        </a>
        <a href="#contato" class="flex items-center gap-3 px-4 py-3 rounded-lg text-sm font-medium text-bluice-100 hover:bg-bluice-800 hover:text-white transition-colors" @click="closeDrawer">
          <span class="text-lg">📧</span> Contato
        </a>
      </nav>

      <!-- Drawer footer -->
      <div class="border-t border-bluice-700 p-4 mt-4 space-y-2">
        <a href="https://github.com/profmugomes" target="_blank" rel="noopener noreferrer"
           class="flex items-center gap-3 px-4 py-3 rounded-lg text-sm font-medium text-bluice-100 hover:bg-bluice-800 hover:text-white transition-colors">
          <span class="text-lg">🐙</span> GitHub
        </a>
        <a href="https://youtube.com/@profmugomes" target="_blank" rel="noopener noreferrer"
           class="flex items-center gap-3 px-4 py-3 rounded-lg text-sm font-semibold text-white bg-emerald-600 hover:bg-emerald-700 transition-colors">
          <span class="text-lg">▶️</span> YouTube
        </a>
      </div>
    </aside>
  </header>
</template>

<script>
export default {
  name: 'AppHeader',
  data() {
    return {
      drawerOpen: false,
    }
  },
  methods: {
    openDrawer() {
      this.drawerOpen = true
      document.body.style.overflow = 'hidden'
    },
    closeDrawer() {
      this.drawerOpen = false
      document.body.style.overflow = ''
    },
  },
}
</script>
