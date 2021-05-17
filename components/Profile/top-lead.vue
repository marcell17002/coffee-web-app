<template>
  <div class="md:w-1/2 md:mx-16 mt-14 md:mt-10 ">
    <div class="flex justify-center">
      <img class="left-0 top-0 mt-10  md:mt-0 w-40 h-40 rounded-full  filter object-cover" :src="require(`@/assets/img/${img}`)">
    </div>
    <h1 class="text-gray-700 text-center md:text-2xl text-xl font-bold pt-5 ">
      {{ name }}
    </h1>
    <h1 class="text-gray-600 pt-1 text-center md:text-lg  text-md font-normal">
      {{ position }}
    </h1>
    <p class="desc">
      {{ description }}
    </p>
  </div>
</template>
<script>
export default {
  props: {
    img: {
      type: String,
      default: null
    },
    name: {
      type: String,
      default: null
    },
    position: {
      type: String,
      default: null
    },
    description: {
      type: String,
      default: null
    }
  }
}
</script>
