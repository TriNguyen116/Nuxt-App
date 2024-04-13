<template>
  <div>
    <a href="#" @click="view('home')">Home</a>
    <a href="#" @click="view('counter')">Counter</a>

    <LazyHomeWelcome v-if="page === 'home'"/>
    <LazyCounter v-if="page === 'counter'"/>
    <NuxtPage/>

  </div>
</template>

<script setup>
  const page = ref("");
  function view(name){
    page.value = name
  }
</script>
