<template>
  <div class="portfolio-item">
    <img :src="image" alt="">
    <h3>{{ title }}</h3>
    <p>{{ description }}</p>
    <div class="social-icons">
      <a href="#" class="facebook"><i class="fab fa-facebook"></i></a>
      <a href="#" class="whatsapp"><i class="fab fa-whatsapp"></i></a>
      <a href="#" class="instagram"><i class="fab fa-instagram"></i></a>
      <a href="#" class="github"><i class="fab fa-github"></i></a>
      <a href="#" class="linkedin"><i class="fab fa-linkedin"></i></a>
      <a href="#" class="youtube"><i class="fab fa-youtube"></i></a>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    image: String,
    title: String,
    description: String,
  }
}
</script>

<style scoped>
.social-icons {
  position: fixed; 
  bottom: 150px; 
  left: 50px; 
  display: flex;
  justify-content: center;
}

.social-icons a {
  margin: 0 10px;
  color: #fff; 
  font-size: 24px; 
  transition: color 0.3s; 
}


.facebook:hover { color: #3b5998; } 
.whatsapp:hover { color: #25D366; } 
.instagram:hover { color: #E1306C; } 
.github:hover { color: #211F1F; } 
.linkedin:hover { color: #0077B5; } 
.youtube:hover { color: #FF0000; } 
</style>
