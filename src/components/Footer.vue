<template>
  <footer class="bg-bluice-950 border-t border-bluice-800">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-8 py-10">
      <div class="flex flex-col sm:flex-row items-center justify-between gap-4">
        <div class="flex items-center gap-2 text-sm text-bluice-300">
          <span class="w-6 h-6 rounded bg-bluice-800 flex items-center justify-center text-white text-xs font-bold">M</span>
          <span>&copy; {{ year }} Murilo Gomes. Todos os direitos reservados.</span>
        </div>
        <div class="flex gap-6 text-sm text-bluice-400">
          <a href="https://youtube.com/@profmugomes" target="_blank" rel="noopener noreferrer" class="hover:text-white transition-colors">YouTube</a>
          <a href="https://github.com/profmugomes" target="_blank" rel="noopener noreferrer" class="hover:text-white transition-colors">GitHub</a>
          <a href="mailto:mugomesoficial@gmail.com" class="hover:text-white transition-colors">Contato</a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'AppFooter',
  data() {
    return {
      year: new Date().getFullYear()
    }
  }
}
</script>
