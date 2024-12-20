<template>
    <div v-if="visible" class="loading-screen">
      <div class="dots">
        <div class="dot"></div>
        <div class="dot"></div>
        <div class="dot"></div>
      </div>
    </div>
  </template>
  
  <script lang="ts">
  import { defineComponent } from 'vue';
  
  export default defineComponent({
    name: 'LoadingScreen',
    props: {
      visible: {
        type: Boolean,
        required: true
      }
    }
  });
  </script>
  
  <style scoped>
  .loading-screen {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.8);
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 1000;
  }
  
  .dots {
    display: flex;
    align-items: center;
  }
  
  .dot {
    width: 10px;
    height: 10px;
    background-color: white;
    border-radius: 50%;
    margin: 0 5px;
    animation: dot-flashing 1s infinite linear alternate;
  }
  
  @keyframes dot-flashing {
    0% {
      opacity: 100;
    }
    50%{
      opacity: 0;
    }
  }
  </style>
  