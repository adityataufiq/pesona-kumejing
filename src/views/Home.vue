<template>
  <div>
    <Hero id="beranda"/>
    <Tentang id="tentang"/>
    <Galeri id="galeri"/>
    <Fasilitas id="fasilitas"/>
    <Paket id="paket"/>
    <Kontak id="kontak"/>
    <Footer id="footer"/>
  </div>
</template>

<script>
  import Hero from '../components/Hero'
  import Tentang from '../components/Tentang'
  import Galeri from '../components/Galeri'
  import Fasilitas from '../components/Fasilitas'
  import Paket from '../components/Paket'
  import Kontak from '../components/Kontak'
  import Footer from '../components/Footer'

  export default {
    name: 'Home',

    components: {
      Hero,
      Tentang,
      Galeri,
      Fasilitas,
      Paket,
      Kontak,
      Footer,
    },
  }
</script>
