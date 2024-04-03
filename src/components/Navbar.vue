<template>
  <div>
    <nav class="logo">
      <h1><span class="my-text">MY</span> PORTFOLIO</h1>
    </nav>
    <nav class="navbar">
      <ul>
        <li><a href="/">HOME</a></li>
        <li><a href="/skill">SKILL</a></li>
        <li><a href="/About.vue">ABOUT</a></li>
        <li><a href="/contact">CONTACT</a></li>
      </ul>
    </nav>
  </div>
</template>


<script>
export default {
 
}
</script>

<style scoped>
.logo {
  position: fixed;
  top: 20px;
  left: 20px;
  z-index: 9999;
  font-family: 'Arial', sans-serif;
}

.logo h1 {
  margin: 0;
  font-size: 36px;
  color: #fff;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
}

.my-text {
  color: #da7f08;
  font-family: 'Pacifico', cursive; 
}

.navbar {
  background-color: transparent;
  color: #fff;
  padding: 10px;
  position: fixed;
  top: 0;
  right: 0;
  border-radius: 10px; 
  box-shadow: 0 2px 4px rgba(63, 1, 1, 0.1); 
}

.navbar ul {
  list-style-type: none;
  padding: 0;
  margin: 0;
  margin-right: 40px;
}

.navbar ul li {
  display: inline;
  margin-right: 30px;
  transition: border-color 0.3s; 
  border-radius: 10px; 
  border: 2px solid transparent; 
}

.navbar ul li:hover {
  border-color: #da7f08; 
}

.navbar ul li:last-child {
  margin-right: 0;
}

.navbar ul li a {
  color: #fff;
  text-decoration: none;
  padding: 10px; 
}

.navbar ul li a:hover {
  color: #da7f08; 
}
</style>
