<template>
    <div class="container">
      <button class="more-button" @click="scrollToAbout">More</button>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      scrollToAbout() {
        const aboutElement = document.getElementById('about');
        if (aboutElement) {
          aboutElement.scrollIntoView({ behavior: 'smooth' });
        }
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
    color: #ffffff; 
    background-color: #ff5722; 
    border: none;
    border-radius: 50px; 
    cursor: pointer;
    outline: none; 
    transition: background-color 0.3s ease, transform 0.2s ease, box-shadow 0.3s ease;
    box-shadow: 0px 4px 6px rgba(255, 87, 34, 0.3); 
    opacity: 0; 
    animation: appearButton 1s ease forwards, shadowPulse 2s infinite alternate; 
  }
  
  .more-button:hover {
    background-color: #ff8a65; 
    transform: translateY(-2px); 
    box-shadow: 0px 6px 8px rgba(255, 87, 34, 0.5); 
  }
  
  @keyframes appearButton {
    from {
      opacity: 0;
      transform: translateY(20px); 
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
  
  @keyframes shadowPulse {
    from {
      box-shadow: 0px 4px 6px rgba(255, 87, 34, 0.3); 
    }
    to {
      box-shadow: 0px 8px 12px rgba(255, 87, 34, 0.6); 
    }
  }
  </style>
  