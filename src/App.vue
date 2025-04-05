<script setup>
import { ref, computed } from 'vue'
import Footer from './components/Footer.vue'
import Header from './components/Header.vue'
import JustifiedTextSection from './components/JustifiedTextSection.vue'
import LinkItem from './components/LinkItem.vue'
import Navbar from './components/Navbar.vue'
import Separator from './components/Separator.vue'
import PagePočetna from '../views/PagePočetna.vue'
import PageSlika from '../views/PageSlika.vue'
import PageGrafika from '../views/PageGrafika.vue'

const activeLink = ref("POČETNA")

const currentPage = computed(() => {
  switch (activeLink.value) {
    case 'SLIKA':
      return PageSlika
    case 'GRAFIKA':
      return PageGrafika
    default:
      return PagePočetna
  }
})
</script>


<template>
    <div class="fixed w-full h-full flex justify-center poppins text-sm text-indigo-300
        bg-gradient-to-b from-[#1B1A55] via-[#2B428D] to-[#3B39BB]">

        <div style="background-image: url('./src/assets/images/pattern.jpg'); 
            background-size: 200px;"
            class="fixed w-full h-full bg-repeat opacity-[3%] -z-10"></div>

        <div class="bg-[#535C91]/25 border-x border-[#9290C3]/10 w-[700px] max-w-[700px] shadow-lg
            flex flex-col justify-between px-8 gap-4 overflow-auto">
        <Header />
        <Navbar :activeLink="activeLink" @update:activeLink="activeLink=$event"/>
        <component :is="currentPage"/>
        <Footer />            
        </div>
    </div>
</template>

