<template>
  <div>
    <Header />
    <!-- <div class="flex justify-center h-52  -mt-2 ">
      <img class="w-full  object-cover " src="~/assets/img/turvis-top.png">
    </div> -->
    <div class="max-w-screen-xl mx-auto ">
      <div class="mx-5 sm:mx-10">
        <div class="flex  pt-10">
          <div class=" hidden sm:flex w-1/2 sm:w-2/5 lg:w-1/3">
            <img class=" h-28 w-full sm:h-full rounded-2xl md:rounded-3xl  filter object-cover " src="~/assets/img/home-step-4.jpg">
          </div>
          <div class="sm:w-1/2 sm:ml-10 lg:ml-20">
            <div class="flex  items-center md:justify-start">
              <h1 class="text-2xl md:text-3xl  md:text-left text-green-700 font-bold">
                Our New Product
              </h1>
              <div class="animate-bounce mt-2   relative text-yellow-400 font-semibold border-2 px-2 border-yellow-400 rounded-md ml-7 ">
                Favorite
              </div>
            </div>
            <h1 class="text-xl  md:text-left text-green-600 font-semibold mt-2">
              Kopi Khas Gunung Halu
            </h1>
            <div class="sm:hidden mt-5">
              <img class=" h-1/3 w-full md:h-full rounded-2xl md:rounded-3xl  filter object-cover " src="~/assets/img/home-step-4.jpg">
            </div>
            <p class="text-gray-500 pt-3 md:text-lg text-md font-light">
              It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old. Richard McClintock, a Latin professor at Hampden-Sydney College in Virginia, looked up one of the more obscure Latin words, consectetur, from a Lorem Ipsum passage, and going through the cites of the word in classical literature, discovered the undoubtable source. Lorem Ipsum comes from sections 1.10.32 and 1.10.33 of "de Finibus Bonorum et Malorum" (The Extremes of Good and Evil) by Cicero, written in 45 BC. This book is a treatise on the theory of ethics, very popular during the Renaissance. The first line of Lorem Ipsum, "Lorem ipsum dolor sit amet..", comes from a line in section 1.10.32.
            </p>
            <button class="mb-5 bg-green-600 text-white text-lg font-semibold border-2 border-green-600 rounded-md px-4 py-1 uppercase mt-10 md:mt-20 lg:mt-32 ">
              <a target="_blank" href="https://linktr.ee/Senjanoesantaracoffee">
                Pesan Sekarang</a>
            </button>
          </div>
        </div>
      </div>

      <div class="pt-20 md:pt-52 mb-10">
        <h1 class="headline mx-5">
          Lorem ipsum dolor sit amet,FRST
        </h1>

        <div class="grid grid-cols-3 gap-2 pt-20 justify-items-center">
          <cards-product
            v-for="product in products"
            :key="product.id"
            :is-merged="product.id=== 5"
            :payload="product"
            :name="product.name"
            :category="product.category"
            :price="product.price"
            :img="product.img"
          />
        </div>

        <div class="mx-5 lg:flex lg:justify-evenly flex-row py-20 md:pt-32 md:px-10 items-center">
          <div>
            <h1 class="lg:absolute text-green-700 font-bold text-3xl">
              What others say about our coffee
            </h1>
            <p class="text-gray-500 pt-2 lg:pt-14 md:text-md text-sm font-light">
              Discover what those who have ventured on the journey have to say.
            </p>
            <div class="hidden lg:flex  mt-20 ">
              <button class="flex bg-green-600 text-white text-lg font-semibold focus:outline-none border-2 border-green-600 rounded-md px-4 py-1 uppercase mt-10 md:mt-20 lg:mt-32 " @click="previous">
                <
              </button>
              <button class="flex ml-10 bg-green-600 text-white text-lg focus:outline-none font-semibold border-2 border-green-600 rounded-md px-4 py-1 uppercase mt-10 md:mt-20 lg:mt-32 " @click="next">
                >
              </button>
            </div>
          </div>

          <div class=" flex lg:justify-end justify-center ">
            <div class=" max-w-xs md:max-w-screen-md -pt-10 sm:-pl-32 ">
              <transition-group class="flex justify-center items-center overflow-hidden" tag="div">
                <div v-for="slide in slides" :key="slide.id" v-touch:swipe.left="previous" v-touch:swipe.right="next" class=" transition ease-in py-10 duration-150 ">
                  <div class="w-96 md:ml-10 flex px-10  items-start md:mt-10 bg-white h-full p-5 rounded-lg shadow md:shadow-lg">
                    <img class="mt-10 border-4 border-green-500 md:mt-0 w-20 h-20 rounded-full  object-cover" :src="require(`@/assets/img/${slide.images}`)">
                    <div class="ml-5">
                      <h1 class="text-gray-700  md:text-lg text-md font-bold">
                        {{ slide.name }}
                      </h1>
                      <h1 class="text-gray-600 pt-1  md:text-md  text-sm font-normal">
                        {{ slide.position }}
                      </h1>
                      <p class="text-gray-500 pt-2   text-sm font-light">
                        {{ slide.description }}
                      </p>
                    </div>
                  </div>
                </div>
              </transition-group>
            </div>
          </div>
          <div class=" lg:hidden  flex justify-between  mt-2 ">
            <button class="flex bg-green-600 text-white text-lg font-semibold focus:outline-none border-2 border-green-600 rounded-md px-4 py-1 uppercase mt-10 md:mt-20 lg:mt-32 " @click="previous">
              <
            </button>
            <button class="flex ml-10 bg-green-600 text-white text-lg focus:outline-none font-semibold border-2 border-green-600 rounded-md px-4 py-1 uppercase mt-10 md:mt-20 lg:mt-32 " @click="next">
              >
            </button>
          </div>
        </div>

        <!-- <div class="pt-20 md:pt-52 mb-10">
      <h1 class="headline">
        Lorem ipsum dolor sit amet, consectetur
      </h1>
      <div class="md:pt-20 flex justify-between  items-center ">
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
    </div> -->
      </div>
    </div>

    <div class="flex md:pt-20">
      <div class="w-2/3  bg-yellow-100 p-5 md:p-10 ">
        <h1 class="md:text-lg text-md text-center md:text-left text-green-700 font-semibold pt-3 ">
          #BangkitBersamaUMKM #KopiSatu
        </h1>
        <h1 class="md:text-3xl text-xl text-center md:text-left text-green-600 font-semibold mt-3 ">
          Rasakan racikan terbaik dari biji pilihan kopi Indonesia
        </h1>
        <p class="text-gray-500 pt-5  md:text-md text-xs md:text-sm font-light">
          Reza telah berkiprah di dunia keuangan dan investasi selama lebih dari 20 tahun. Penulis beberapa buku mengenai keuangan dan investasi; 6 Seri "50 Financial Wisdom" dan "Berwisata ke Dunia Reksadana".
        </p>
        <button class="bg-green-600 text-white text-sm md:text-lg font-semibold border-2 border-green-600 rounded-md px-4 py-1 uppercase mt-10 md:mt-20 lg:mt-32 ">
          <a target="_blank" class="href=&quot;https://linktr.ee/Senjanoesantaracoffee&quot;">
            Pesan Sekarang</a>
        </button>
      </div>
      <div class="w-1/3">
        <img class="w-full h-full object-cover " src="~/assets/img/home-step-4.jpg">
      </div>
    </div>

    <Footer />
    <getButton />
  </div>
</template>
<script>
import Vue from 'vue'
import Vue2TouchEvents from 'vue2-touch-events'
import data from './data'

Vue.use(Vue2TouchEvents)
export default {
  data () {
    return {
      products: data,
      slides: [{
        id: 1,
        images: 'about-avatar-2.jpg',
        name: 'Yustinus S.',
        position: 'CEO of E-Fishery',
        description: 'Reza telah berkiprah di dunia keuangan dan investasi selama lebih dari 20 tahun. Penulis beberapa buku mengenai keuangan dan investasi; 6 Seri "50 Financial Wisdom" dan "Berwisata ke Dunia Reksadana.'
      },
      {
        id: 2,
        images: 'about-avatar-3.jpg',
        name: 'Marko Palandini',
        position: 'Staff of Angkasa Pura 1',
        description: 'Reza telah berkiprah di dunia keuangan dan investasi selama lebih dari 20 tahun. Penulis beberapa buku mengenai keuangan dan investasi; 6 Seri "50 Financial Wisdom" dan "Berwisata ke Dunia Reksadana.'
      },
      {
        id: 3,
        images: 'about-avatar-3.jpg',
        name: 'Marcell Antonius',
        position: 'CTO of Buyyo.id',
        description: 'Reza telah berkiprah di dunia keuangan dan investasi selama lebih dari 20 tahun. Penulis beberapa buku mengenai keuangan dan investasi; 6 Seri "50 Financial Wisdom" dan "Berwisata ke Dunia Reksadana.'
      },
      {
        id: 4,
        images: 'about-avatar-4.jpg',
        name: 'Jane Luckman Haris',
        position: 'Staff of Marketing BCA ',
        description: 'Reza telah berkiprah di dunia keuangan dan investasi selama lebih dari 20 tahun. Penulis beberapa buku mengenai keuangan dan investasi; 6 Seri "50 Financial Wisdom" dan "Berwisata ke Dunia Reksadana.'
      },
      {
        id: 5,
        images: 'about-avatar-5.jpg',
        name: 'Pratama Dinureja',
        position: 'Marketing Intern Readyleanr',
        description: 'Reza telah berkiprah di dunia keuangan dan investasi selama lebih dari 20 tahun. Penulis beberapa buku mengenai keuangan dan investasi; 6 Seri "50 Financial Wisdom" dan "Berwisata ke Dunia Reksadana.'
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
