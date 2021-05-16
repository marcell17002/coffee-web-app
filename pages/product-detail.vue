<template>
  <div>
    <Header />
    <div class="max-w-screen-xl mx-auto ">
      <div class="mx-5 pt-5 md:pt-20 mb-10">
        <div class="flex lg:pr-20 lg:ml-11">
          <div class=" hidden sm:flex w-1/2 sm:w-2/5 lg:w-1/3">
            <img class=" h-28 w-full sm:h-full rounded-2xl md:rounded-3xl  filter object-cover " src="~/assets/img/home-step-2.jpg">
          </div>
          <div class=" sm:w-1/2  sm:ml-10 lg:ml-10  ">
            <div class="flex  items-center justify-between">
              <h1 class="text-2xl md:text-3xl  md:text-left text-green-700 font-bold">
                Our New Product
              </h1>
              <div class="mt-2  relative text-red-400 font-semibold border-2 px-2 border-red-400 rounded-md ml-7 ">
                35 000
              </div>
            </div>
            <h1 class="text-xl  md:text-left text-green-600 font-semibold mt-2">
              Kopi Khas Gunung Halu
            </h1>
            <div class="flex justify-start items-center mt-5 ">
              <div class="flex">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5  mr-3 md:mr-4 ml-1 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 4a1 1 0 011-1h16a1 1 0 011 1v2.586a1 1 0 01-.293.707l-6.414 6.414a1 1 0 00-.293.707V17l-4 4v-6.586a1 1 0 00-.293-.707L3.293 7.293A1 1 0 013 6.586V4z" />
                </svg>
                <h2 class="text-xs md:text-sm  text-gray-900">
                  Semi-washed
                </h2>
              </div>
              <div class="flex md:ml-2 ">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5  mr-3 md:mr-4 ml-1 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14.828 14.828a4 4 0 01-5.656 0M9 10h.01M15 10h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z" />
                </svg>
                <h2 class="text-xs md:text-sm  text-gray-900">
                  Light to Medium
                </h2>
              </div>
              <div class="flex md:ml-2">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5  mr-3 md:mr-4 ml-1 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 10h4.764a2 2 0 011.789 2.894l-3.5 7A2 2 0 0115.263 21h-4.017c-.163 0-.326-.02-.485-.06L7 20m7-10V5a2 2 0 00-2-2h-.095c-.5 0-.905.405-.905.905 0 .714-.211 1.412-.608 2.006L7 11v9m7-10h-2M7 20H5a2 2 0 01-2-2v-6a2 2 0 012-2h2.5" />
                </svg>
                <h2 class="text-xs md:text-sm  text-gray-900">
                  <span class="text-green-600 font-bold"> 100 % </span> Arabika
                </h2>
              </div>
              <div class="flex md:ml-2">
                <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5  mr-3 md:mr-4 ml-1 text-green-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                </svg>
                <h1 class="text-xs md:text-sm  text-gray-900">
                  Pangalengan, Bandung
                </h1>
              </div>
            </div>
            <div class="sm:hidden mt-5 flex justify-center ">
              <img class="md:h-full w-full h-80 rounded-md  object-cover " src="~/assets/img/home-product.jpg">
            </div>
            <p class="text-gray-500 pt-5 md:text-lg text-md font-light">
              It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old. Richard McClintock, a Latin professor at Hampden-Sydney College in Virginia, looked up one of the more obscure Latin words, consectetur, from a Lorem Ipsum passage, and going through the cites of the word in classical literature, discovered the undoubtable source. Lorem Ipsum comes from sections 1.10.32 and 1.10.33 of "de Finibus Bonorum et Malorum" (The Extremes of Good and Evil) by Cicero, written in 45 BC.
            </p>
            <button class="mb-5 bg-green-600 text-white text-lg font-semibold border-2 border-green-600 rounded-md px-4 py-1 uppercase mt-10  ">
              Pesan Sekarang
            </button>
          </div>
        </div>
      </div>
    </div>
    <div class="pt-20 md:pt-20 mb-10">
      <h1 class="text-2xl px-5 md:text-3xl xl:px-18 md:px-14 tracking-wide text-gray-700 font-bold md:text-center">
        Our Suggestion
      </h1>
      <div class="md:pt-10 flex justify-between  items-center ">
        <div class="relative flex justify-center w-full  ">
          <button class=" ml-2 absolute left-0  mt-48 h-8 w-8 rounded-full p-2 bg-white text-gray-600 text-xl font-semibold  focus:outline-none    " @click="previous">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7" />
            </svg>
          </button>
          <button class="mr-2 absolute p-2 mt-48 right-0 ml-10 h-8 w-8 rounded-full bg-white text-gray-600 text-xl font-semibold  focus:outline-none    " @click="next">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
            </svg>
          </button>
          <transition-group class="flex   justify-center items-center overflow-hidden" tag="div">
            <div v-for="slide in slides" :key="slide.id" class=" transition ease-in py-10 duration-150 ">
              <div :class="slide.color" class="w-52 shadow-md ml-5 rounded-3xl">
                <div class="p-5">
                  <h1 class="font-bold text-gray-700 text-xl">
                    {{ slide.title }}
                  </h1>
                  <p class="font-light text-gray-700 text-sm pt-3 md:text-md ">
                    {{ slide.description }}
                  </p>
                </div>
                <img class="mt-14 w-full  h-32 rounded-b-3xl filter object-cover " src="~/assets/img/home-step-4.jpg">
              </div>
            </div>
          </transition-group>
        </div>
      </div>
    </div>
    <Footer />
  </div>
</template>
<script>
export default {
  data () {
    return {
      slides: [{
        id: 1,
        color: 'bg-green-100',
        images: 'about-avatar-2',
        title: 'Si Hitam Manis Rinjani ',
        description: 'racikan mantap dari lembah di ujung Rinjani'
      }, {
        id: 2,
        color: 'bg-yellow-200',
        images: 'about-avatar-2',
        title: 'Serbuk Kopi Pilihan Gn. Halu  ',
        description: 'Melalui prosesan yang rapih dari petani'
      }, {
        id: 3,
        color: 'bg-green-200',
        images: 'about-avatar-2',
        title: 'Kopi dengan aroma pilihan ',
        description: 'kopi khas ciwidey dengan proses sederhana'
      }, {
        id: 1,
        color: 'bg-gray-200',
        images: 'about-avatar-2',
        title: 'Si Hitam Manis Rinjani ',
        description: 'racikan mantap dari lembah di ujung Rinjani'
      }, {
        id: 2,
        color: 'bg-yellow-200',
        images: 'about-avatar-2',
        title: 'Serbuk Kopi Pilihan dari ',
        description: 'Melalui prosesan yang rapih dari petani'
      }, {
        id: 3,
        color: 'bg-gray-200',
        images: 'about-avatar-2',
        title: 'Si Hitam Manis Rinjai ',
        description: 'racikan mantap dari lembah di ujung Rinjani'
      }, {
        id: 3,
        color: 'bg-yellow-100',
        images: 'about-avatar-2',
        title: 'Si Hitam Manis Rinjai ',
        description: 'racikan mantap dari lembah di ujung Rinjani'
      }]
    }
  },
  methods: {
    next () {
      const first = this.slides.shift()
      this.slides = this.slides.concat(first)
    },
    previous () {
      const last = this.slides.pop()
      this.slides = [last].concat(this.slides)
    }
  }
}
</script>
