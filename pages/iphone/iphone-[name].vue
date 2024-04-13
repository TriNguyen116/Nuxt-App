<template>
  <div>
    <Head>
      <Title>Nuxt 3 - Iphone {{ name }}</Title>
    </Head>
    <div class="flex justify-center w-full mt-20">
      <div class="grid grid-cols-2">
        <div>
          <img :src="`/images/iphone-${route.params.name}.jpg`" width="200" height="200" />
        </div>
        <div class="text-center">
          <h1 class="text-3xl">Iphone {{ name }}</h1>
          <button
            @click="addToCart"
            class="p-3 bg-indigo-900 text-white rounded-md mt-5 w-48"
          >
            <span v-if="isInCart()">Remove from Cart </span>
            <span v-else>Buy Now </span>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
  const route = useRoute();
   const name = computed(()=>
    {
      return route.params.name.replace("-"," ");
    }
  )
  const fullname = computed(()=>
    {
      return `iphone-${route.params.name}`;
    }
  )
    const cart = useCart()

    function isInCart(){
      return !!cart.value.find((ct) => ct.name === fullname.value);
    }

  function addToCart(){
    if(!isInCart()){
      cart.value.push({
      name: fullname,
    })
    console.log(cart.value)
    } else {
      cart.value = cart.value.filter((ct)=>ct.name !== fullname.value);
      console.log(fullname.value)
      console.log(cart.value)
      
    }
  }
  // useHead({
  //   title: `Nuxt3 - ${route.params.name}`
  // })
</script>