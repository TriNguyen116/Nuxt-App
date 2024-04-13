<template>
  <div class="grid grid-cols-4 gap-4 mt-10">
    <nuxt-link to="/iphone/iphone-12" class="shadow-lg text-center border rounded-lg p-5">
      <h1>Iphone 12</h1>
      <div class="flex justify-center ">
        <img src="public/images/iphone-12.jpg" alt="" width="100" height="100">
      </div>
    </nuxt-link>
    <nuxt-link to="/iphone/iphone-12-pro" class="shadow-lg text-center  border rounded-lg p-5">
      <h1>Iphone 12 pro</h1>
      <div class="flex justify-center">
      <img src="/public/images/iphone-12-pro.jpg" alt="" width="100" height="100">
    </div>
    </nuxt-link>
    <nuxt-link to="/iphone/iphone-13" class="shadow-lg text-center  border rounded-lg p-5">
      <h1>Iphone 13</h1>
      <div class="flex justify-center">
      <img src="/public/images/iphone-13.jpg" alt="" width="100" height="100">
    </div>
    </nuxt-link>
    <nuxt-link to="/iphone/iphone-13-pro" class="shadow-lg text-center  border rounded-lg p-5">
      <h1>Iphone 13 pro</h1>
      <div class="flex justify-center">
      <img src="/public/images/iphone-13-pro.jpg" alt="" width="100" height="100">
    </div>
    </nuxt-link>
  </div>
</template>

<script setup>
  useHead({
    title: "Nuxt3 - Iphones",
  })
</script>