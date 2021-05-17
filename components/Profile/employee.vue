<template>
  <div class=" md:mx-10 mt-14 md:mt-10 ">
    <div class="flex justify-center">
      <img class=" mt-10  md:mt-0 w-36 h-36 rounded-full  filter object-cover" :src="require(`@/assets/img/${img}`)">
    </div>
    <h1 class="text-gray-700 text-center md:text-2xl text-xl font-semibold pt-5 ">
      {{ name }}
    </h1>
    <h1 class="text-gray-600 pt-1 text-center md:text-md  text-md font-normal">
      {{ position }}
    </h1>
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
    }
  }
}
</script>
