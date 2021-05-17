<template>
  <nuxt-link :to="{name:'product-detail',params:{payload}}" :class="isMerged ? 'col-span-2 lg:mr-10' : ''" class="p-5 shadow-sm">
    <div class=" flex sm:hidden justify-end my-2 ">
      <div v-if="category === 'Baru'" class="animate-bounce text-green-400 text-xs md:text-md font-bold border-2 px-2 border-green-400 rounded-md ">
        Baru
      </div>
      <div v-else-if="category === 'Bundle'" class=" text-blue-400 text-xs md:text-md font-bold border-2 px-2 border-green-400 rounded-md ">
        Bundle
      </div>
      <div v-else-if="category === 'Hot'" class=" text-red-400 text-xs md:text-md font-bold border-2 px-2 border-green-400 rounded-md ">
        HOT
      </div>
      <div v-else class=" text-yellow-400 text-xs md:text-md font-bold border-2 px-2 border-yellow-400 rounded-md ">
        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-yellow-400" viewBox="0 0 20 20" fill="currentColor">
          <path d="M2 10.5a1.5 1.5 0 113 0v6a1.5 1.5 0 01-3 0v-6zM6 10.333v5.43a2 2 0 001.106 1.79l.05.025A4 4 0 008.943 18h5.416a2 2 0 001.962-1.608l1.2-6A2 2 0 0015.56 8H12V4a2 2 0 00-2-2 1 1 0 00-1 1v.667a4 4 0 01-.8 2.4L6.8 7.933a4 4 0 00-.8 2.4z" />
        </svg>
      </div>
    </div>
    <div class="flex justify-center">
      <img :class="isMerged ? 'w-screen' : ''" class=" h-28  md:h-60 rounded-2xl md:rounded-md  filter object-cover" :src="require(`@/assets/img/${img}`)">
    </div>
    <div class="flex justify-between items-center">
      <div class="flex pt-5">
        <div>
          <h1 class="text-green-800 text-xs md:text-lg font-semibold ">
            {{ name }}
          </h1>
          <h1 class="font-semibold pt-3 text-xs md:text-sm text-green-500">
            {{ price }}
          </h1>
        </div>
      </div>
      <div class="hidden sm:flex sm:mb-2">
        <div v-if="category === 'Baru'" class=" animate-bounce relative text-sm text-green-400 font-semibold border-2 px-2 border-green-400 rounded-md ml-7 ">
          Baru
        </div>
        <div v-else-if="category === 'Bundle'" class=" relative text-sm text-blue-400 font-semibold border-2 px-2 border-blue-400 rounded-md ml-7 ">
          Bundle
        </div>
        <div v-else-if="category === 'Hot'" class=" relative text-sm text-red-400 font-semibold border-2 px-2 border-red-400 rounded-md ml-7 ">
          HOT
        </div>
        <div v-else class=" relative text-sm text-yellow-400 font-semibold border-2 px-2 border-yellow-400 rounded-md ml-7">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-yellow-400" viewBox="0 0 20 20" fill="currentColor">
            <path d="M2 10.5a1.5 1.5 0 113 0v6a1.5 1.5 0 01-3 0v-6zM6 10.333v5.43a2 2 0 001.106 1.79l.05.025A4 4 0 008.943 18h5.416a2 2 0 001.962-1.608l1.2-6A2 2 0 0015.56 8H12V4a2 2 0 00-2-2 1 1 0 00-1 1v.667a4 4 0 01-.8 2.4L6.8 7.933a4 4 0 00-.8 2.4z" />
          </svg>
        </div>
      </div>
    </div>
  </nuxt-link>
</template>
<script>
export default {
  props: {
    payload: {
      type: Object,
      default: null
    },
    isMerged: {
      type: Boolean,
      default: null
    },
    name: {
      type: String,
      default: null
    },
    price: {
      type: Number,
      default: null
    },
    category: {
      type: String,
      default: null
    },
    img: {
      type: String,
      default: null
    }
  }
}
</script>
