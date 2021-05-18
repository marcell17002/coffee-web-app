<template>
  <div class="md:h-52 md:w-1/3 h-56 mt-32 md:-mt-0  md:ml-7">
    <img class=" h-full w-full md:h-full rounded-2xl md:rounded-3xl   object-cover " :src="require(`@/assets/img/${img}`)">
    <h1 class="text-gray-700 text-md font-semibold  pt-5">
      {{ title }}
    </h1>
    <h1 class="text-sm  md:text-md mt-2 text-gray-700  font-normal md:text-justify">
      {{ description }}
    </h1>
  </div>
</template>
<script>
export default {
  props: {
    img: {
      type: String,
      default: 'hello'
    },
    title: {
      type: String,
      default: 'hello'
    },
    description: {
      type: String,
      default: 'hello'
    }
  }
}
</script>
