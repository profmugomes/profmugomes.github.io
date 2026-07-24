<template>
  <section id="sobre" class="py-16 lg:py-24 bg-white">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="max-w-3xl mx-auto text-center">
        <span class="text-emerald-600 font-semibold text-sm uppercase tracking-wider">Sobre</span>
        <h2 class="mt-2 text-3xl sm:text-4xl font-bold text-bluice-900">Prof Mu Gomes</h2>
        <p class="mt-4 text-lg text-slate-500 leading-relaxed">
          Programador há <strong class="text-slate-700">21 anos</strong>, sendo
          <strong class="text-slate-700">14 anos</strong> dedicados ao PHP e
          <strong class="text-slate-700">10 anos</strong> atuando ativamente no
          ecossistema de <strong class="text-slate-700">software livre</strong>.
          No YouTube, compartilho conhecimento sobre PHP, código aberto e tecnologia
          no canal <a href="https://youtube.com/@profmugomes" target="_blank" rel="noopener noreferrer"
                      class="text-emerald-600 hover:text-emerald-700 font-semibold">@profmugomes</a>.
        </p>
      </div>

      <div class="mt-12 grid sm:grid-cols-3 gap-8 text-center">
        <div class="p-6">
          <div class="w-14 h-14 mx-auto rounded-2xl bg-bluice-100 flex items-center justify-center text-2xl">💻</div>
          <h3 class="mt-4 text-lg font-bold text-slate-800">Código Aberto</h3>
          <p class="mt-2 text-sm text-slate-500">
            10 anos contribuindo com projetos open source e comunidades de software livre.
          </p>
        </div>
        <div class="p-6">
          <div class="w-14 h-14 mx-auto rounded-2xl bg-emerald-100 flex items-center justify-center text-2xl">🐘</div>
          <h3 class="mt-4 text-lg font-bold text-slate-800">PHP desde 2010</h3>
          <p class="mt-2 text-sm text-slate-500">
            14 anos de experiência com PHP, criando sistemas, frameworks e ferramentas robustas.
          </p>
        </div>
        <div class="p-6">
          <div class="w-14 h-14 mx-auto rounded-2xl bg-violet-100 flex items-center justify-center text-2xl">🎬</div>
          <h3 class="mt-4 text-lg font-bold text-slate-800">YouTube & Palestras</h3>
          <p class="mt-2 text-sm text-slate-500">
            Conteúdo sobre tecnologia no YouTube e palestras como no PHP Manaus.
          </p>
        </div>
      </div>
    </div>
  </section>

  <!-- Blog placeholder -->
  <section id="blog" class="py-16 lg:py-20 bg-slate-50">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="max-w-xl mx-auto text-center">
        <span class="text-emerald-600 font-semibold text-sm uppercase tracking-wider">Em Breve</span>
        <h2 class="mt-2 text-3xl sm:text-4xl font-bold text-bluice-900">Blog</h2>
        <p class="mt-4 text-lg text-slate-500 leading-relaxed">
          Artigos, tutoriais e insights sobre PHP, software livre, otimização de sistemas
          e tudo que envolve o universo da programação.
        </p>
        <div class="mt-8 inline-flex items-center gap-3 px-6 py-3 rounded-xl bg-bluice-900 text-bluice-200 text-sm font-medium">
          <span class="w-2 h-2 rounded-full bg-amber-400 animate-pulse"></span>
          Em desenvolvimento — em breve novidades
        </div>
      </div>
    </div>
  </section>

  <!-- Loja placeholder -->
  <section id="loja" class="py-16 lg:py-20 bg-white">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="max-w-xl mx-auto text-center">
        <span class="text-emerald-600 font-semibold text-sm uppercase tracking-wider">Em Breve</span>
        <h2 class="mt-2 text-3xl sm:text-4xl font-bold text-bluice-900">Loja Virtual</h2>
        <p class="mt-4 text-lg text-slate-500 leading-relaxed">
          Cursos, consultorias e produtos digitais para quem quer aprofundar
          seus conhecimentos em PHP, desenvolvimento de sistemas e tecnologias abertas.
        </p>
        <div class="mt-8 inline-flex items-center gap-3 px-6 py-3 rounded-xl bg-emerald-100 text-emerald-700 text-sm font-medium">
          <span class="w-2 h-2 rounded-full bg-emerald-500 animate-pulse"></span>
          Em desenvolvimento — em breve novidades
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'AppAbout'
}
</script>
