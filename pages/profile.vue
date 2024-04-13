<template>
  <p>Profile</p>

 <!-- replace cotent by sidebar -->
<slot></slot>
</template>

<script setup>
  definePageMeta({
    layout: 'sidebar',
  })
</script>