<template>
  <section class="relative overflow-hidden bg-gradient-to-br from-bluice-900 via-bluice-800 to-bluice-950">
    <!-- Grid pattern overlay -->
    <div class="absolute inset-0 opacity-10" style="background-image: url('data:image/svg+xml,%3Csvg width=\'60\' height=\'60\' viewBox=\'0 0 60 60\' xmlns=\'http://www.w3.org/2000/svg\'%3E%3Cg fill=\'none\' fill-rule=\'evenodd\'%3E%3Cg fill=\'%23ffffff\' fill-opacity=\'0.15\'%3E%3Ccircle cx=\'30\' cy=\'30\' r=\'1\'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E');"></div>

    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-20 lg:py-28 relative">
      <div class="max-w-3xl mx-auto text-center">
        <!-- Badge YouTube -->
        <a href="https://youtube.com/@profmugomes" target="_blank" rel="noopener noreferrer"
           class="inline-flex items-center gap-2 px-4 py-1.5 rounded-full bg-emerald-500/15 text-emerald-300 text-sm font-medium mb-6 hover:bg-emerald-500/25 transition-colors">
          <span class="w-2 h-2 rounded-full bg-emerald-400 animate-pulse"></span>
          youtube.com/@profmugomes
        </a>

        <!-- Título -->
        <h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-white leading-tight">
          Prof Mu Gomes<br>
          <span class="text-emerald-400">21 anos de programação</span>
        </h1>

        <div class="mt-10 flex flex-col sm:flex-row gap-4 justify-center">
          <a href="#projetos"
             class="inline-flex items-center justify-center px-8 py-3.5 rounded-xl bg-emerald-600 hover:bg-emerald-700 text-white font-semibold text-base shadow-lg shadow-emerald-600/25 transition-all hover:shadow-emerald-600/40">
            Ver Projetos
            <svg class="ml-2 w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7l5 5m0 0l-5 5m5-5H6"/></svg>
          </a>
          <a href="#sobre"
             class="inline-flex items-center justify-center px-8 py-3.5 rounded-xl bg-white/10 hover:bg-white/20 text-white font-semibold text-base border border-white/20 transition-colors">
            Sobre Mim
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'AppHero'
}
</script>
