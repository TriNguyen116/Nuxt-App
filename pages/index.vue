<template>
  <div>
    This is Home
 
  <button @click="moveToAbout" >Take me to About Page</button>
  </div>
  
</template>

<script setup>
  function moveToAbout(){
    navigateTo("about")
  }

</script>