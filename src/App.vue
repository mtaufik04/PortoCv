<template>
  <div id="app">
    <Navbar />
    <div class="portfolio">
      <PortfolioItem 
        v-for="(item, index) in portfolioItems"
        :key="index"
        :image="item.image"
        :title="item.title"
        :description="item.description"
      />
      <img alt="vue gambar" class="rounded-image" src="./assets/download.jpeg">
    </div>
    
    <keterangan /> 
    <Buttomd/>
    <About/>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import PortfolioItem from './components/PortfolioItem.vue'
import keterangan from './components/keterangan.vue'
import Buttomd from './components/Buttomd.vue' 
import About from './components/About.vue' 

export default {
  components: {
    Navbar,
    PortfolioItem,
    keterangan, 
    Buttomd,
    About
  },
  data() {
    return {
      portfolioItems: [
        {
         
        }
      ]
    }
  }
}
</script>

<style>
.rounded-image {
  margin-top: 50px;
  border-radius: 50%;
  width: 300px;
  height: 300px;
  object-fit: cover;
  float: left;
  margin-right: 800px;
  margin-left: -100px;
  border: 4px solid rgb(70, 42, 169);
  box-shadow: 0px 0px 20px 0px rgba(70, 42, 169, 0.5);
 
}
</style>
