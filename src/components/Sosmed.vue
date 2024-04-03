<template>
  <div class="social-icons">
    <a href="#" class="facebook"><i class="fab fa-facebook"></i></a>
    <a href="#" class="whatsapp"><i class="fab fa-whatsapp"></i></a>
    <a href="#" class="instagram"><i class="fab fa-instagram"></i></a>
    <a href="#" class="github"><i class="fab fa-github"></i></a>
    <a href="#" class="linkedin"><i class="fab fa-linkedin"></i></a>
    <a href="#" class="youtube"><i class="fab fa-youtube"></i></a>
  </div>
</template>

<script>
export default {
  // add functionality if needed
}
</script>

<style scoped>
.social-icons {
  position: fixed; /* Menggunakan posisi tetap */
  bottom: 130px; /* Menempatkan ikon di bawah */
  left: 30px; /* Menempatkan ikon di kiri */
  display: flex;
  justify-content: center;
}

.social-icons a {
  margin: 0 10px;
  color: #fff; /* Warna default ikon */
  font-size: 24px; /* Sesuaikan ukuran ikon */
  transition: color 0.3s; /* Animasi perubahan warna */
}

/* Efek hover untuk masing-masing ikon */
.facebook:hover { color: #3b5998; } /* Warna biru saat dihover */
.whatsapp:hover { color: #25D366; } /* Warna hijau saat dihover */
.instagram:hover { color: #E1306C; } /* Warna merah saat dihover */
.github:hover { color: #211F1F; } /* Warna hitam saat dihover */
.linkedin:hover { color: #0077B5; } /* Warna biru laut saat dihover */
.youtube:hover { color: #FF0000; } /* Warna merah saat dihover */
</style>
