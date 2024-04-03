<template>
    <div class="container">
      <div id="about">
        <h2>About Me</h2>
        <div class="content">
          <img alt="gambar" class="rounded-image" src="../assets/download1.jpeg">
          <div class="paragraphs">
            <p>
              Perkenalkan, nama saya M.TAUFIK KURRAHMAN, panggilan saya Taufik. Saat ini saya menempuh pendidikan di Universitas Islam Riau tepatnya di Kota Pekanbaru, Riau. Saya berasal dari Bagansiapiapi dan memiliki 4 orang saudara. Saya adalah anak tertua dan lahir serta besar di Bagansiapiapi. Riwayat sekolah saya dimulai dari SDN 006 Bagan Barat, kemudian melanjutkan ke SMPN 2 Bangko, dan SMAN 1 Bangko. Saya Memilih Jurusan  Teknik Informatika di uir.
            </p>
            <p>
              Untuk pengalaman, saya masih dalam tahap pembelajaran di dunia IT ini dan belum memiliki pengalaman yang cukup. Oleh karena itu, saya terus belajar hingga memahami pemecahan dalam penyelesaian masalah dalam pemrograman. Untuk skill, saya sedang belajar bahasa pemrograman seperti JavaScript, Python, SQL, C++, dan Java.
            </p>
            <div class="skills">
              <p class="skill-text">My Skills:</p>
            
              <i class="fab fa-python bordered" title="Python"></i>
              
              <i class="fab fa-css3-alt bordered" title="CSS"></i>
        
              <i class="fab fa-js bordered" title="JavaScript"></i>
            
              <i class="fas fa-database bordered" title="Database"></i>
             
              <i class="fab fa-java bordered" title="Java"></i>
            </div>
          </div>
        </div>
      </div>
      <button class="more-button" @click="scrollToAbout" v-show="showMoreButton">More</button>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        showMoreButton: true 
      };
    },
    mounted() {
      window.addEventListener('scroll', this.handleScroll); 
    },
    beforeDestroy() {
      window.removeEventListener('scroll', this.handleScroll); 
    },
    methods: {
      scrollToAbout() {
        const aboutElement = document.getElementById('about');
        if (aboutElement) {
          aboutElement.scrollIntoView({ behavior: 'smooth' });
        }
      },
      handleScroll() {
     
        this.showMoreButton = window.scrollY === 0;
      }
    }
  };
  </script>
  
  <style scoped>
  .container {
    display: flex;
    justify-content: center; 
    align-items: center; 
    height: 100vh;
  }
  
  .more-button {
    padding: 10px 20px;
    font-size: 18px;
    font-weight: bold;
    color: #d50808;
    background-color: transparent;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    transition: background-color 0.3s ease, transform 0.2s ease, box-shadow 0.3s ease;
    box-shadow: 0px 4px 6px rgba(93, 1, 1, 0.6); 
  }
  
  .more-button:hover {
    background-color: #9d9c9c;
    transform: translateY(-2px);
    box-shadow: 0px 6px 8px rgba(93, 1, 1, 0.8); 
  }
  
  .rounded-image {
    max-width: 40%; 
    border-radius: 10px; 
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1); 
    float: left;
    margin-right: 30px;
    margin-left: -100px;
  }
  
  .content {
    display: flex; 
    align-items: center; 
  }
  
  .paragraphs {
    max-width: 70%; 
  }
  
  .paragraphs p {
    text-align: justify;
  }
  
  .bordered {
    font-size: 30px;
    margin-right: 40px;
  }
  
  .skill-text {
    font-weight: bold;
    margin-bottom: 10px;
  }
  </style>
  