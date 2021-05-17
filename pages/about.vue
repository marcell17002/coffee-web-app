<template>
  <div>
    <Header />
    <div class="max-w-screen-xl mx-auto ">
      <div class="mx-5">
        <h1 class="text-2xl md:text-3xl pt-10 tracking-wide text-gray-700 font-bold">
          Welcoming a fresh start
        </h1>
        <div class="md:flex md:justify-between items-center md:mr-10 mt-10 ">
          <div>
            <p class="desc">
              Contrary to popular belief, Lorem Ipsum is not simply random text.
            </p>
            <p class="desc">
              It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old. Richard McClintock, a Latin professor at Hampden-Sydney College in Virginia, looked up one of the more obscure Latin words, consectetur, from a Lorem Ipsum passage, and going through the cites of the word in classical literature, discovered the undoubtable source. Lorem Ipsum comes from sections 1.10.32 and 1.10.33 of "de Finibus Bonorum et Malorum" (The Extremes of Good and Evil) by Cicero, written in 45 BC. This book is a treatise on the theory of ethics, very popular during the Renaissance. The first line of Lorem Ipsum, "Lorem ipsum dolor sit amet..", comes from a line in section 1.10.32.
            </p>
            <br>
            <p class="desc">
              The standard chunk of Lorem Ipsum used since the 1500s is reproduced below for those interested. Sections 1.10.32 and 1.10.33 from "de Finibus Bonorum et Malorum" by Cicero are also reproduced in their exact original form, accompanied by English versions from the 1914 translation by H. Rackham.
            </p>
            <br>
            <p class="desc">
              exact original form, accompanied by English versions from the 1914 translation by H. Rackham.
            </p>
          </div>
          <img class=" mt-10 md:mt-0 h-80 w-full md:h-1/3 lg:h-64 rounded-2xl md:rounded-3xl  filter object-cover md:ml-20" src="~/assets/img/home-product.jpg">
        </div>
        <div class="pt-20 md:pt-20">
          <h1 class="headline">
            Meet with our teams
          </h1>
          <div class=" md:flex md:justify-evenly flex-row justify-center  md:mx-20  md:mt-20">
            <profile-top-lead name="Reza Zakaria" img="about-avatar-1.jpg" position="CEO & Co-Founder" description=" Reza telah berkiprah di dunia keuangan dan investasi selama lebih dari 20 tahun. Penulis beberapa buku mengenai keuangan dan investasi; 6 Seri '50 Financial Wisdom' dan 'Berwisata ke Dunia Reksadana'." />
            <profile-top-lead name="Jesica Ling" img="about-avatar-3.jpg" position="Chairman & Co-Founders" description=" Reza telah berkiprah di dunia keuangan dan investasi selama lebih dari 20 tahun. Penulis beberapa buku mengenai keuangan dan investasi; 6 Seri '50 Financial Wisdom' dan 'Berwisata ke Dunia Reksadana'." />
          </div>

          <div class=" md:flex md:justify-evenly flex-row justify-center  md:mx-20 pb-20 md:mt-20">
            <profile-employee v-for="profile in profiles" :key="profile.id" :img="profile.img" :name="profile.name" :position="profile.position" />
          </div>
        </div>

        <!-- <div class=" pt-20 lg:flex lg:justify-evenly flex-row py-20 md:pt-20 md:px-10 items-center">
          <div>
            <h1 class="text-green-700 font-bold text-3xl">
              What others say about us
            </h1>
            <p class="text-gray-500 pt-2  md:text-md text-sm font-light">
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
            <div class=" max-w-xs md:max-w-2xl -pt-10 sm:-pl-32 ">
              <transition-group class="flex justify-center items-center overflow-hidden" tag="div">
                <div v-for="slide in slides" :key="slide.id" class=" transition ease-in py-10 duration-150 ">
                  <div class="w-96 lg:ml-10 flex ml-4  items-start md:mt-10 bg-white h-full p-5 rounded-lg shadow-lg">
                    <img class="mt-10 border-4 border-green-500 md:mt-0 w-20 h-20 rounded-full  object-cover" :src="'~/assets/img/'+slide.img+'.jpg'">
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
        </div> -->
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
      profiles: [
        {
          id: 2,
          img: 'about-avatar-7.jpg',
          name: 'Marko Palandini',
          position: 'Staff of Angkasa Pura 1',
          description: 'Reza telah berkiprah di dunia keuangan dan investasi selama lebih dari 20 tahun. Penulis beberapa buku mengenai keuangan dan investasi; 6 Seri "50 Financial Wisdom" dan "Berwisata ke Dunia Reksadana.'
        },
        {
          id: 3,
          img: 'about-avatar-2.jpg',
          name: 'Marcell Antonius',
          position: 'CTO of Buyyo.id',
          description: 'Reza telah berkiprah di dunia keuangan dan investasi selama lebih dari 20 tahun. Penulis beberapa buku mengenai keuangan dan investasi; 6 Seri "50 Financial Wisdom" dan "Berwisata ke Dunia Reksadana.'
        },
        {
          id: 4,
          img: 'about-avatar-4.jpg',
          name: 'Jane Luckman Haris',
          position: 'Staff of Marketing BCA ',
          description: 'Reza telah berkiprah di dunia keuangan dan investasi selama lebih dari 20 tahun. Penulis beberapa buku mengenai keuangan dan investasi; 6 Seri "50 Financial Wisdom" dan "Berwisata ke Dunia Reksadana.'
        },
        {
          id: 5,
          img: 'about-avatar-5.jpg',
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
