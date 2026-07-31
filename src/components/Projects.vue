<template>
  <section id="projetos" class="py-16 lg:py-24 bg-slate-50">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8">
      <!-- Título -->
      <div class="text-center mb-14">
        <span class="text-emerald-600 font-semibold text-sm uppercase tracking-wider">Portfólio</span>
        <h2 class="mt-2 text-3xl sm:text-4xl font-bold text-bluice-900">Meus Projetos</h2>
        <p class="mt-4 text-lg text-slate-500 max-w-2xl mx-auto">
          Projetos autorais e contribuições open source que desenvolvi ao longo da carreira.
        </p>
      </div>

      <!-- Projetos (fixos) -->
      <div class="mb-12">
        <h3 class="text-xl font-bold text-slate-700 mb-6 flex items-center gap-2">
          <span class="text-2xl">📌</span> Projetos
        </h3>
        <div class="grid sm:grid-cols-2 lg:grid-cols-3 gap-6">
          <a v-for="p in autorais" :key="p.name" :href="p.url" target="_blank" rel="noopener noreferrer"
             class="group bg-white rounded-xl border border-slate-200 p-6 hover:shadow-lg hover:border-bluice-200 transition-all duration-300">
            <div class="text-3xl mb-4">{{ p.icon }}</div>
            <h4 class="text-lg font-bold text-slate-800 group-hover:text-bluice-700 transition-colors">{{ p.name }}</h4>
            <p class="mt-2 text-sm text-slate-500 leading-relaxed">{{ p.desc }}</p>
          </a>
        </div>
      </div>

      <!-- Repositórios do GitHub -->
      <div>
        <h3 class="text-xl font-bold text-slate-700 mb-6 flex items-center gap-2">
          <span class="text-2xl">📦</span> Repositórios no GitHub
        </h3>

        <!-- Estado de loading -->
        <div v-if="loading" class="grid sm:grid-cols-2 lg:grid-cols-3 gap-6">
          <div v-for="n in 6" :key="n"
               class="bg-white rounded-xl border border-slate-200 p-6 animate-pulse">
            <div class="h-5 bg-slate-200 rounded w-3/4 mb-4"></div>
            <div class="h-4 bg-slate-200 rounded w-full mb-2"></div>
            <div class="h-4 bg-slate-200 rounded w-2/3"></div>
          </div>
        </div>

        <!-- Estado de erro -->
        <div v-else-if="error" class="text-center py-10">
          <p class="text-slate-400 text-lg mb-2">😕 Não foi possível carregar os repositórios</p>
          <p class="text-sm text-slate-400">{{ error }}</p>
        </div>

        <!-- Grid de repositórios -->
        <div v-else class="grid sm:grid-cols-2 lg:grid-cols-3 gap-6">
          <a v-for="repo in repos" :key="repo.id" :href="repo.html_url" target="_blank" rel="noopener noreferrer"
             class="group bg-white rounded-xl border border-slate-200 p-6 hover:shadow-lg hover:border-bluice-200 transition-all duration-300">
            <div class="flex items-center gap-2 mb-3">
              <h4 class="text-base font-bold text-slate-800 group-hover:text-bluice-700 transition-colors truncate">
                {{ repo.name }}
              </h4>
              <svg class="w-4 h-4 flex-shrink-0 text-slate-300 group-hover:text-bluice-400 transition-colors" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"/>
              </svg>
            </div>
            <p class="text-sm text-slate-500 leading-relaxed line-clamp-2 min-h-[2.5rem]">
              {{ repo.description || 'Sem descrição' }}
            </p>
            <div class="mt-4 flex items-center gap-4 text-xs text-slate-400">
              <span v-if="repo.language" class="flex items-center gap-1.5">
                <span class="w-2.5 h-2.5 rounded-full" :style="{ backgroundColor: langColor(repo.language) }"></span>
                {{ repo.language }}
              </span>
              <span v-if="repo.stargazers_count > 0" class="flex items-center gap-1">
                ⭐ {{ repo.stargazers_count }}
              </span>
              <span class="ml-auto">
                {{ timeAgo(repo.updated_at) }}
              </span>
            </div>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
const LANG_COLORS = {
  PHP: '#777BB4',
  JavaScript: '#f1e05a',
  TypeScript: '#3178c6',
  Python: '#3572A5',
  Go: '#00ADD8',
  HTML: '#e34c26',
  CSS: '#563d7c',
  Shell: '#89e051',
  Vue: '#41b883',
  Dart: '#00B4AB',
  C: '#555555',
  'C++': '#f34b7d',
  Ruby: '#701516',
  Java: '#b07219',
  Rust: '#dea584',
}

export default {
  name: 'AppProjects',
  data() {
    return {
      autorais: [
        {
          name: 'BluMegaOS',
          desc: 'Sistema operacional Linux otimizado para desempenho e produtividade.',
          icon: '🖥️',
          url: 'https://github.com/profmugomes',
        },
        {
          name: 'Kubuntu Brasil',
          desc: 'Site oficial da comunidade Kubuntu Brasil.',
          icon: '🌐',
          url: 'https://github.com/profmugomes',
        },
        {
          name: 'LifeFriends',
          desc: 'Rede social focada em conexões genuínas entre pessoas.',
          icon: '👥',
          url: 'https://github.com/profmugomes',
        },
        {
          name: 'BluIce Browser',
          desc: 'Navegador baseado em WebKit com foco em privacidade e performance.',
          icon: '🌍',
          url: 'https://github.com/profmugomes',
        },
        {
          name: 'Palestra PHP Manaus',
          desc: 'Palestra sobre PHP e IA apresentada no canal PHP Manaus.',
          icon: '🎤',
          url: 'https://github.com/profmugomes',
        },
        {
          name: 'CleanSafe',
          desc: 'Software de limpeza e otimização para sistemas Linux.',
          icon: '🧹',
          url: 'https://github.com/profmugomes',
        },
      ],
      repos: [],
      loading: true,
      error: null,
    }
  },
  mounted() {
    this.fetchRepos()
  },
  methods: {
    async fetchRepos() {
      try {
        const res = await fetch('https://api.github.com/users/profmugomes/repos?sort=updated&per_page=20&type=owner')
        if (!res.ok) throw new Error(`GitHub API retornou ${res.status}`)
        const data = await res.json()
        this.repos = data.filter(r => !r.fork)
      } catch (e) {
        this.error = e.message
      } finally {
        this.loading = false
      }
    },
    langColor(lang) {
      return LANG_COLORS[lang] || '#6b7280'
    },
    timeAgo(date) {
      const diff = Date.now() - new Date(date).getTime()
      const days = Math.floor(diff / 86400000)
      if (days === 0) return 'hoje'
      if (days === 1) return 'há 1 dia'
      if (days < 30) return `há ${days} dias`
      const months = Math.floor(days / 30)
      if (months === 1) return 'há 1 mês'
      return `há ${months} meses`
    }
  }
}
</script>
