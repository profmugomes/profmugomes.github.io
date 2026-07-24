<template>
  <div id="app" class="min-h-screen bg-slate-50 text-slate-800">
    <Header />
    <main>
      <Hero />
      <Projects />
      <About />
      <Contact />
    </main>
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Hero from './components/Hero.vue'
import Projects from './components/Projects.vue'
import About from './components/About.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Hero,
    Projects,
    About,
    Contact,
    Footer,
  }
}
</script>
