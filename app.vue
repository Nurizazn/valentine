<template>
  <div class="container">
    <h1 class="valentine-title">Valentine's Day</h1>
    <div class="cards-container">
      <div v-for="(valentine, index) in valentineMessages" :key="index" class="card">
        <img :src="valentine.image" alt="Heart Image" class="heart-image" />
        <h2>{{ valentine.title }}</h2>
        <p class="message">{{ valentine.message }}</p>
        <p class="sender">{{ valentine.sender }}</p>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const valentineMessages = ref([
  {
    title: "First",
    message: "Heyyo, Selamat tanggal 14 Februari!\nHappy Valentine's Day yaa!",
    sender: "-Fana",
    image: "/satu.jpg"
  },
  {
    title: "Second",
    message: "Today is a special day, right? \nA special day with a special person, namely you.\nThank you for being the best of the best friends here. I'm grateful to be able to meet and get to know you here. Even though we meet virtually, I love you very much.",
    sender: "-Fana",
    image: "/dua.jpg"
  },
  {
    title: "Third",
    message: "May your day be full of love and happiness, be happy! Don't forget to smile a lot for the day and beyond. And may we be friends forever and meet on the next Valentine's Day!",
    sender: "-Fana",
    image: "/tiga.jpg"
  }
]);
</script>

<style scoped>
html, body {
  height: 100%;
  margin: 0;
  padding: 0;
}

.container {
  min-height: 100vh; /* Pastikan container penuh layar */
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: #ffccd5;
  font-family: Arial, sans-serif;
  padding: 20px;
}

.valentine-title {
  text-align: center;
  font-size: 36px;
  color: #d63384;
  font-weight: bold;
  margin-bottom: 20px;
}

.cards-container {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  gap: 20px;
  max-width: 80%;
}

.card {
  background: white;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.2);
  text-align: center;
  max-width: 300px;
  transition: transform 0.3s ease;
}

.card:hover {
  transform: scale(1.05);
}

.heart-image {
  width: 200px;
  height: 200px;
  object-fit: cover;
  margin-bottom: 10px;
  border-radius: 50%;
}

h2 {
  font-size: 20px;
  color: #d63384;
  margin-bottom: 5px;
}

.message {
  font-size: 16px;
  margin: 15px 0;
  color: #333;
}

.sender {
  font-size: 14px;
  font-style: italic;
  color: #555;
}
</style>
