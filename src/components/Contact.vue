<template>
  <section id="contato" class="py-16 lg:py-24 bg-gradient-to-br from-bluice-900 via-bluice-800 to-bluice-950 relative overflow-hidden">
    <div class="absolute inset-0 opacity-5" style="background-image: url('data:image/svg+xml,%3Csvg width=\'60\' height=\'60\' viewBox=\'0 0 60 60\' xmlns=\'http://www.w3.org/2000/svg\'%3E%3Cg fill=\'none\' fill-rule=\'evenodd\'%3E%3Cg fill=\'%23ffffff\' fill-opacity=\'0.15\'%3E%3Ccircle cx=\'30\' cy=\'30\' r=\'1\'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E');"></div>

    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 relative">
      <div class="text-center mb-14">
        <span class="text-emerald-400 font-semibold text-sm uppercase tracking-wider">Contato</span>
        <h2 class="mt-2 text-3xl sm:text-4xl font-bold text-white">Onde me encontrar</h2>
        <p class="mt-4 text-lg text-bluice-200 max-w-xl mx-auto">
          Acompanhe meu trabalho, assista aos vídeos ou entre em contato.
        </p>
      </div>

      <div class="grid sm:grid-cols-2 lg:grid-cols-4 gap-6 max-w-4xl mx-auto">
        <!-- YouTube -->
        <a href="https://youtube.com/@profmugomes" target="_blank" rel="noopener noreferrer"
           class="group bg-white/10 hover:bg-white/20 backdrop-blur rounded-xl border border-white/10 p-6 text-center transition-all duration-300">
          <div class="w-14 h-14 mx-auto rounded-2xl bg-red-500/20 flex items-center justify-center text-3xl mb-4">
            ▶️
          </div>
          <h3 class="text-white font-bold">YouTube</h3>
          <p class="text-sm text-bluice-200 mt-1">@profmugomes</p>
        </a>

        <!-- GitHub -->
        <a href="https://github.com/profmugomes" target="_blank" rel="noopener noreferrer"
           class="group bg-white/10 hover:bg-white/20 backdrop-blur rounded-xl border border-white/10 p-6 text-center transition-all duration-300">
          <div class="w-14 h-14 mx-auto rounded-2xl bg-slate-500/20 flex items-center justify-center text-3xl mb-4">
            🐙
          </div>
          <h3 class="text-white font-bold">GitHub</h3>
          <p class="text-sm text-bluice-200 mt-1">/profmugomes</p>
        </a>

        <!-- Email -->
        <a href="mailto:mugomesoficial@gmail.com"
           class="group bg-white/10 hover:bg-white/20 backdrop-blur rounded-xl border border-white/10 p-6 text-center transition-all duration-300">
          <div class="w-14 h-14 mx-auto rounded-2xl bg-emerald-500/20 flex items-center justify-center text-3xl mb-4">
            ✉️
          </div>
          <h3 class="text-white font-bold">Email</h3>
          <p class="text-sm text-bluice-200 mt-1">mugomesoficial</p>
        </a>

        <!-- LinkedIn -->
        <a href="https://linkedin.com/in/profmugomes" target="_blank" rel="noopener noreferrer"
           class="group bg-white/10 hover:bg-white/20 backdrop-blur rounded-xl border border-white/10 p-6 text-center transition-all duration-300">
          <div class="w-14 h-14 mx-auto rounded-2xl bg-blue-500/20 flex items-center justify-center text-3xl mb-4">
            💼
          </div>
          <h3 class="text-white font-bold">LinkedIn</h3>
          <p class="text-sm text-bluice-200 mt-1">/in/profmugomes</p>
        </a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'AppContact'
}
</script>
