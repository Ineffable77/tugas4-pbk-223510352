<template>
    <div class="container">
      <button @click="goEmit">klik disini</button>
    </div>
  </template>
  
  <script>
export default {
  methods: {
    goEmit() {
      alert("Kerja kalo mau kaya bang hehe");
    },
  },
};
  </script>
  
  <style scoped>
  .container {
    padding: 2rem;
    background-color: #EEF7FF;
    border: 1px solid #bbb;
    border-radius: 5px;
    margin-top: 10px;
  }
  button {
    padding: 1rem 2rem;
    border: none;
    border-radius: 16px;
    background-color: #29bb04;
    color: white;
    cursor: pointer;

  }
  button:hover {
    background-color: #008127;
    transition: 0.5ms;
  }
  </style>
  