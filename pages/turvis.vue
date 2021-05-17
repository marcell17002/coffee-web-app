/* eslint-disable vue/valid-v-for */
<template>
  <div>
    <Header />

    <div class="flex justify-center -mt-2 z-0">
      <img class=" h-80 w-screen md:h-full filter object-cover " src="~/assets/img/turvis-top.png">
    </div>
    <div class="max-w-screen-xl mx-auto ">
      <div class="pt-20 mx-5">
        <h1 class="headline">
          We're driven by stories
        </h1>
        <div class="md:flex md:justify-evenly flex-row  md:mx-20   md:mt-10">
          <div class="mt-10">
            <iframe class="rounded-3xl h-80 w-full" src="https://www.youtube.com/embed/tgbNymZ7vqY?autoplay=0&mute=1" />
            <div class="pt-5 px-3">
              <h1 class="text-md md:text-lg xl:px-18  tracking-wide text-gray-700 font-bold ">
                "I want to see my design changing the world. And this was a step closer."
              </h1>
              <h1 class="text-sm md:text-md xl:px-18 pt-3 tracking-wide text-gray-700 font-normal ">
                Fatema, Product Designer
              </h1>
            </div>
          </div>
          <div class="mt-10 md:ml-10">
            <iframe class="rounded-3xl h-80 w-full" src="https://www.youtube.com/embed/tgbNymZ7vqY?autoplay=0&mute=1" />
            <div class="pt-5 px-3">
              <h1 class="text-md md:text-lg xl:px-18  tracking-wide text-gray-700 font-bold ">
                "I want to see my design changing the world. And this was a step closer."
              </h1>
              <h1 class="text-sm md:text-md xl:px-18  pt-3 tracking-wide text-gray-700 font-normal ">
                Fatema, Product Designer
              </h1>
            </div>
          </div>
        </div>
      </div>
      <div class="pt-20 md:pt-32 mx-5">
        <h1 class="text-2xl md:text-3xl xl:px-18 md:px-14 tracking-wide text-gray-700 font-bold md:text-center">
          Heating up with our  <span class="text-red-500 ">new</span> coffee area in colaborating with <span class="text-green-700 ">Ciwidey Farmer's</span>
        </h1>
        <div class="grid grid-cols-4 gap-4 mt-20">
          <div class="...">
            <img class=" h-28 w-screen md:h-60 rounded-2xl md:rounded-3xl  filter object-cover " src="~/assets/img/home-step-1.jpg">
          </div>
          <div class="...">
            <img class=" h-28 w-screen md:h-60 rounded-2xl md:rounded-3xl  filter object-cover " src="~/assets/img/home-step-2.jpg">
          </div>
          <div class="col-span-2 ...">
            <img class=" h-28 w-screen md:h-60 filter rounded-2xl md:rounded-3xl  object-cover " src="~/assets/img/home-step-3.jpg">
          </div>

          <div class="col-span-2 ...">
            <img class=" h-28 w-screen md:h-60 filter rounded-2xl md:rounded-3xl  object-cover " src="~/assets/img/home-step-4.jpg">
          </div>
          <div class="...">
            <img class=" h-28 w-screen md:h-60 filter rounded-2xl md:rounded-3xl  object-cover " src="~/assets/img/turvis-card-1.jpg">
          </div>
          <div class="...">
            <img class=" h-28 w-screen md:h-60 filter rounded-2xl md:rounded-3xl  object-cover " src="~/assets/img/turvis-card-2.jpeg">
          </div>

          <div class="...">
            <img class=" h-28 w-screen md:h-60 filter rounded-2xl md:rounded-3xl  object-cover " src="~/assets/img/turvis-card-3.jpg">
          </div>
          <div class="col-span-2 ...">
            <img class=" h-28 w-screen md:h-60 filter rounded-2xl md:rounded-3xl  object-cover " src="~/assets/img/turvis-card-4.jpg">
          </div>
          <div class="...">
            <img class=" h-28 w-screen md:h-60 filter rounded-2xl md:rounded-3xl  object-cover " src="~/assets/img/turvis-card-5.jpg">
          </div>
        </div>
      </div>
      <div class="pt-20 md:pt-32 mb-64 mx-5">
        <h1 class="headline">
          Lorem ipsum dolor sit amet, consectetusrasds
        </h1>
        <div>
          <div class=" md:flex md:justify-evenly flex-row  md:mx-20  md:mt-32">
            <cards-turvis v-for="item in itemsOne" :key="item.id" :img="item.img" :title="item.title" :description="item.description" />
          </div>
          <div class=" md:flex md:justify-evenly flex-row  md:mx-20  md:mt-32">
            <cards-turvis v-for="item in itemsTwo" :key="item.id" :img="item.img" :title="item.title" :description="item.description" />
          </div>
        </div>
      </div>
    </div>
    <Footer />
    <getButton />
  </div>
</template>
<script>
export default {
  data () {
    return {
      itemsOne: [{
        id: 1,
        img: 'turvis-card-1.jpg',
        title: ' Pemilihan  Kopi Berkualitas  Dari Kebun Desa Pak Sumardi',
        description: 'Pak Sumardi, Ciwidey'
      }, {
        id: 2,
        img: 'turvis-card-2.jpeg',
        title: ' Pemilihan  Kopi Berkualitas  Dari Kebun Desa Pak Sumardi',
        description: 'Pak Sumardi, Ciwidey'
      }, {
        id: 3,
        img: 'turvis-card-3.jpg',
        title: ' Pemilihan  Kopi Berkualitas  Dari Kebun Desa Pak Sumardi',
        description: 'Pak Sumardi, Ciwidey'
      }],
      itemsTwo: [{
        id: 1,
        img: 'turvis-card-4.jpg',
        title: ' Pemilihan  Kopi Berkualitas  Dari Kebun Desa Pak Sumardi',
        description: 'Pak Sumardi, Ciwidey'
      }, {
        id: 2,
        img: 'turvis-card-5.jpg',
        title: ' Pemilihan  Kopi Berkualitas  Dari Kebun Desa Pak Sumardi',
        description: 'Pak Sumardi, Ciwidey'
      }, {
        id: 3,
        img: 'turvis-card-6.jpg',
        title: ' Pemilihan  Kopi Berkualitas  Dari Kebun Desa Pak Sumardi',
        description: 'Pak Sumardi, Ciwidey'
      }]
    }
  }
}
</script>
