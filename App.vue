<script setup>
import {ref} from 'vue';
const  message = ref('Aldenaire Coffe');
const isVisible= ref(true);
const inputText= ref('')
const count = ref(0);
const increment = () => {
  count.value++;
}
</script>

<template>
<h1>{{ message }}</h1>

<img :src="'/images.png'" alt="Logo" :width="200"/>

<button @click="isVisible=!isVisible">Hide</button>
<p v-if="isVisible">Coffe pilihan terbaik since 1998</p>

<input v-model="inputText" placeholder="isi menu.."/>
<p>menu: {{ inputText }}</p>

<button @click="increment">Tambah</button>
<p>jumlah: {{ count }}</p>

</template>

<style>
h1 {
  color: #493308;
}
/* === Global Styles === */
:root {
  --primary-color: #d4a373; /* Warna coklat aesthetic */
  --primary-hover: #b08968;
  --bg-dark: #f5f0e1; /* Warna cream aesthetic */
  --bg-light: #ffffff;
  --text-dark: #5c3d2e; /* Warna coklat gelap */
  --text-light: #3e2723;
  --button-bg: #e6ccb2;
  --button-border-hover: #b08968;

  font-family: "Avenir", "Helvetica", "Arial", sans-serif;
  line-height: 1.5;
  font-weight: 400;
  font-synthesis: none;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  color-scheme: light dark;
  color: var(--text-dark);
  background-color: var(--bg-dark);
}

body {
  margin: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  min-width: 320px;
  min-height: 100vh;
  background: linear-gradient(135deg, #f5ebe0, #f5f0e1);
}

/* === Typography === */
h1 {
  font-size: 3rem;
  font-weight: bold;
  color: var(--primary-color);
  text-align: center;
  margin-bottom: 1rem;
}

p {
  font-size: 1.2rem;
  color: var(--text-dark);
  text-align: center;
}

/* === Links === */
a {
  font-weight: 500;
  color: var(--primary-color);
  text-decoration: none;
  transition: color 0.3s ease;
}

a:hover {
  color: var(--primary-hover);
}

/* === Buttons === */
button {
  display: inline-block;
  padding: 10px 20px;
  font-size: 1rem;
  font-weight: 600;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  background-color: var(--button-bg);
  color: var(--text-dark);
  transition: all 0.3s ease;
}

button:hover {
  background-color: var(--primary-hover);
  transform: scale(1.05);
}

button:focus,
button:focus-visible {
  outline: 4px auto -webkit-focus-ring-color;
}

/* === Image Styling === */
img {
  display: block;
  margin: 20px auto;
  max-width: 100%;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
}

/* === Card Styling === */
.card {
  background: rgba(255, 255, 255, 0.8);
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
  text-align: center;
  max-width: 400px;
  margin: auto;
}

/* === Form Input === */
input {
  width: 100%;
  padding: 10px;
  margin-top: 10px;
  font-size: 1rem;
  border: 2px solid var(--primary-color);
  border-radius: 6px;
  background-color: transparent;
  color: var(--text-dark);
  outline: none;
  transition: all 0.3s ease;
}

input::placeholder {
  color: rgba(0, 0, 0, 0.5);
}

input:focus {
  border-color: var(--primary-hover);
  transform: scale(1.02);
}

/* === Container Styling === */
#app {
  max-width: 600px;
  margin: 0 auto;
  padding: 2rem;
  text-align: center;
}

/* === Responsive Design === */
@media (max-width: 768px) {
  h1 {
    font-size: 2.5rem;
  }

  p {
    font-size: 1rem;
  }

  button {
    font-size: 0.9rem;
  }
}

@media (prefers-color-scheme: dark) {
  :root {
    color: var(--text-light);
    background-color: #3e2723;
  }
  a:hover {
    color: var(--primary-hover);
  }
  button {
    background-color: var(--button-bg);
    color: var(--text-light);
  }
}

</style>
