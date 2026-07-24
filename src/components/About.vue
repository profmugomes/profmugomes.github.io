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

  <!-- Assinantes -->
  <section id="assinantes" class="py-16 lg:py-20 bg-slate-50">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center">
        <span class="text-emerald-600 font-semibold text-sm uppercase tracking-wider">Apoie</span>
        <h2 class="mt-2 text-3xl sm:text-4xl font-bold text-bluice-900">Assinantes</h2>
        <p class="mt-4 text-lg text-slate-500 leading-relaxed max-w-xl mx-auto">
          Ajude a manter o conteúdo gratuito e tenha acesso a salas exclusivas, materiais
          e benefícios especiais.
        </p>
      </div>

      <div class="mt-12 grid sm:grid-cols-2 lg:grid-cols-3 gap-8">
        <!-- SalaPHP -->
        <div class="bg-white rounded-2xl p-6 shadow-sm border border-slate-200 flex flex-col items-center text-center hover:shadow-md transition-shadow">
          <div class="w-16 h-16 rounded-2xl bg-bluice-100 flex items-center justify-center text-3xl">🐘</div>
          <h3 class="mt-4 text-xl font-bold text-slate-800">SalaPHP</h3>
          <p class="mt-2 text-sm text-slate-500 leading-relaxed">
            Sala de aula no Google Classroom com conteúdo premium,
            suporte e networking com a comunidade PHP. É necessário ter
            uma <strong>conta do Google</strong> para acessar.
          </p>
          <a href="https://pag.ae/81_94G9G4" target="_blank" rel="noopener noreferrer"
             class="mt-5 inline-flex items-center gap-2 text-sm font-semibold text-white bg-emerald-600 hover:bg-emerald-700 transition-colors px-5 py-2.5 rounded-lg shadow-sm">
            Assinar SalaPHP
            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"/>
            </svg>
          </a>
        </div>

        <!-- Placeholder para futuros assinantes -->
        <div class="bg-white rounded-2xl p-6 shadow-sm border border-slate-200 border-dashed flex flex-col items-center justify-center text-center min-h-[260px] opacity-60 hover:opacity-80 transition-opacity">
          <div class="w-12 h-12 rounded-full bg-slate-100 flex items-center justify-center text-2xl">➕</div>
          <p class="mt-3 text-sm font-medium text-slate-400">Novos grupos em breve</p>
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
