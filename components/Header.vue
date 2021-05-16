<template>
  <div class="my-5 max-w-screen-xl  mx-auto z-20">
    <div class="flex items-center justify-between ml-5">
      <div class="flex">
        <img class="h-20" src="~/assets/img/logo.png">
        <div class="ml-20 hidden md:block md:-ml-4 lg:ml-4">
          <ul class="flex p-5">
            <nuxt-link to="/">
              <li class="ml-5 text-xl hover:text-green-900 text-gray-500 hover:border-green-900 border-transparent border-b-2 pb-5 ">
                Home
              </li>
            </nuxt-link>
            <nuxt-link to="turvis">
              <li class="ml-5 text-xl hover:text-green-900 text-gray-500 hover:border-green-900 border-transparent border-b-2 pb-5 ">
                Virtual Tour
              </li>
            </nuxt-link>
            <nuxt-link to="shop">
              <li class="ml-5 text-xl hover:text-green-900 text-gray-500 hover:border-green-900 border-transparent border-b-2 pb-5 ">
                Shop
              </li>
            </nuxt-link>
            <nuxt-link to="about">
              <li class="ml-5 text-xl hover:text-green-900 text-gray-500 hover:border-green-900 border-transparent border-b-2 pb-5">
                About
              </li>
            </nuxt-link>
          </ul>
        </div>
      </div>
      <div class="block md:hidden mr-5">
        <button class="flex bg-green-900 text-white hover:text-white items-center border rounded-md p-3 hover:bg-gray-400 focus:outline-none " @click="toggle">
          <svg class="fill-current h-5 w-5" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>Menu</title><path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" /></svg>
        </button>
      </div>

      <div class="mr-10 -mt-5 hidden md:block">
        <div class="flex">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-5 text-green-700 " viewBox="0 0 20 20" fill="currentColor">
            <path fill-rule="evenodd" d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z" clip-rule="evenodd" />
          </svg>
          <h1 class="text-sm  text-gray-900">
            Location : Pangalengan, Bandung
          </h1>
        </div>
        <div class="flex mt-2">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5  mr-4 ml-1 text-green-700" viewBox="0 0 20 20" fill="currentColor">
            <path d="M2 3a1 1 0 011-1h2.153a1 1 0 01.986.836l.74 4.435a1 1 0 01-.54 1.06l-1.548.773a11.037 11.037 0 006.105 6.105l.774-1.548a1 1 0 011.059-.54l4.435.74a1 1 0 01.836.986V17a1 1 0 01-1 1h-2C7.82 18 2 12.18 2 5V3z" />
          </svg>
          <h2 class="text-sm  text-gray-900">
            Call Us : 0895401011469
          </h2>
        </div>
      </div>
    </div>
    <div :class="open ? 'block': 'hidden'" class="w-full md:hidden flex-grow md:items-center md:w-auto px-5 my-10 border-b-2 md:border-b-0 pb-5">
      <div class="text-sm md:flex-grow md:hidden">
        <nuxt-link to="/" class=" block text-xl hover:text-green-900 text-gray-500  pb-5 ">
          Home
        </nuxt-link>
        <nuxt-link to="turvis" class=" block text-xl hover:text-green-900 text-gray-500  pb-5 ">
          Virtual Tour
        </nuxt-link>
        <nuxt-link to="about" class=" block text-xl hover:text-green-900 text-gray-500  pb-5 ">
          About
        </nuxt-link>
        <div class="flex justify-between mt-3">
          <div class="flex">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 mr-5 text-green-700 " viewBox="0 0 20 20" fill="currentColor">
              <path fill-rule="evenodd" d="M5.05 4.05a7 7 0 119.9 9.9L10 18.9l-4.95-4.95a7 7 0 010-9.9zM10 11a2 2 0 100-4 2 2 0 000 4z" clip-rule="evenodd" />
            </svg>
            <h1 class="text-sm  text-gray-900">
              Location : Pangalengan, Bandung
            </h1>
          </div>
          <div class="flex">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5  mr-4 ml-1 text-green-700" viewBox="0 0 20 20" fill="currentColor">
              <path d="M2 3a1 1 0 011-1h2.153a1 1 0 01.986.836l.74 4.435a1 1 0 01-.54 1.06l-1.548.773a11.037 11.037 0 006.105 6.105l.774-1.548a1 1 0 011.059-.54l4.435.74a1 1 0 01.836.986V17a1 1 0 01-1 1h-2C7.82 18 2 12.18 2 5V3z" />
            </svg>
            <h2 class="text-sm  text-gray-900">
              Call Us : 0895401011469
            </h2>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default ({
  data () {
    return {
      open: false
    }
  },
  methods: {
    toggle () {
      this.open = !this.open
    }
  }
})
</script>
