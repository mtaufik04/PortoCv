<template>
  <div class="container">
    <div class="intro-text">
      <p class="welcome-text">Hi, wellcome to my portfolio!</p>
      <p class="typing-text">{{ currentText }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      texts: [
       "I'M M.TAUFIK KURRAHMAN",
        "SAYA  ADALAH SEORANG MAHASISWA UNIVERSITAS ISLAM RIAU"
        
      ],
      currentIndex: 0,
      currentText: ""
    };
  },
  mounted() {
    this.animateText();
  },
  methods: {
    animateText() {
      let index = 0;
      const text = this.texts[this.currentIndex];
      const intervalId = setInterval(() => {
        if (index < text.length) {
          this.currentText += text[index];
          index++;
        } else {
          clearInterval(intervalId);
          setTimeout(() => {
            this.currentText = "";
            this.currentIndex = (this.currentIndex + 1) % this.texts.length;
            this.animateText();
          }, 1000);
        }
      }, 100); 
    }
  }
};
</script>

<style scoped>
.container {
  position: relative;
}

.intro-text {
  position: absolute;
  top: 150px;
  left: 50%;
  transform: translateX(-50%);
  text-align: center;
}

.welcome-text {
  font-size: 24px;
  color: #fff;
  margin-bottom: 20px; 
}

.typing-text {
  font-size: 20px;
  font-weight: bold;
  color: #f8f8f8;
  white-space: nowrap; 
  overflow: hidden; 
  border-right: 0.15em solid orange; 
  animation: typing 1s steps(40, end), blink-caret 0.75s step-end infinite;
}

@keyframes typing {
  from {
    width: 0;
  }
}

@keyframes blink-caret {
  from, to {
    border-color: transparent;
  }
  50% {
    border-color: #2c3e50;
  }
}
</style>
