<template>
  <div class=" bg-green-900">
    <div class="max-w-screen-xl mx-auto p-10 lg:pr-56">
      <nuxt-link to="/">
        <img class="h-20" src="~/assets/img/logo.png">
      </nuxt-link>
      <div class="flex justify-between my-10 flex-wrap">
        <div class="pb-5">
          <h2 class="text-white text-xl mb-5 font-bold">
            Perusahaan
          </h2>
          <ul class="-ml-5">
            <li class="ml-5 text-lg hover:text-white text-gray-300  my-2 ">
              <nuxt-link to="about">
                Tentang
              </nuxt-link>
            </li>
            <li class="ml-5 text-lg hover:text-white text-gray-300  my-2 ">
              <nuxt-link to="turvis">
                Virtual Tour
              </nuxt-link>
            </li>
            <li class="ml-5 text-lg hover:text-white text-gray-300  my-2 ">
              <nuxt-link to="shop">
                Shop
              </nuxt-link>
            </li>
          </ul>
        </div>
        <div class="mr-35 sm:mt-0 sm:mx-auto md:mx-0">
          <h2 class="text-white text-xl mb-5 font-bold">
            Gabung
          </h2>
          <ul class="-ml-5">
            <li class="ml-5 text-lg hover:text-white text-gray-300  my-2 ">
              <a href="https://api.whatsapp.com/send?phone=62812-2455-7760&text=Hello+Reza%2C+saya+ingin+bekerja+sama+dengan+perusahaan+anda">
                Mitra kami
              </a>
            </li>
          </ul>
        </div>
        <div class=" sm:-mt-0 pb-5">
          <h2 class="text-white text-xl  mb-5 font-bold">
            Hubungi Kami
          </h2>
          <div class="flex items-center my-2">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-white  mr-3" viewBox="0 0 20 20" fill="currentColor">
              <path fill-rule="evenodd" d="M14.243 5.757a6 6 0 10-.986 9.284 1 1 0 111.087 1.678A8 8 0 1118 10a3 3 0 01-4.8 2.401A4 4 0 1114 10a1 1 0 102 0c0-1.537-.586-3.07-1.757-4.243zM12 10a2 2 0 10-4 0 2 2 0 004 0z" clip-rule="evenodd" />
            </svg>
            <h3 class="text-gray-300  ">
              marcellantonius18@gmail.com
            </h3>
          </div>
          <div class="flex items-center my-2">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-white mr-3" viewBox="0 0 20 20" fill="currentColor">
              <path fill-rule="evenodd" d="M7 2a2 2 0 00-2 2v12a2 2 0 002 2h6a2 2 0 002-2V4a2 2 0 00-2-2H7zm3 14a1 1 0 100-2 1 1 0 000 2z" clip-rule="evenodd" />
            </svg>
            <h3 class="text-gray-300  ">
              +62 895401011469
            </h3>
          </div>
        </div>

        <div class=" ">
          <h2 class="text-white text-xl  mb-5 font-bold">
            Cari tau update kami
          </h2>
          <div class="flex my-2 justify-around items-center">
            <a href="https://www.instagram.com/arntonius/"><font-awesome-icon class="text-white text-4xl" :icon="['fab', 'facebook']" /></a>
            <a href="https://www.instagram.com/arntonius/"><font-awesome-icon class="text-white text-4xl" :icon="['fab', 'instagram']" /></a>
            <a href="https://www.instagram.com/arntonius/"><font-awesome-icon class="text-white text-4xl" :icon="['fab', 'youtube']" /></a>
          </div>
        </div>
      </div>
      <h3 class="text-white">
        © 2021 Gojek Gojek adalah merek milik PT Aplikasi Karya Anak Bangsa. Terdaftar pada Direktorat Jendral Kekayaan Intelektual Republik Indonesia.
      </h3>
    </div>
  </div>
</template>

<script>
export default {
  sendMail () {
    $.ajax({
      type: 'POST',
      url: 'https://mandrillapp.com/api/1.0/messages/send.json',
      data: {
        key: 'YOUR API KEY HERE',
        message: {
          from_email: 'YOUR@EMAIL.HERE',
          to: [
            {
              email: 'RECIPIENT@EMAIL.HERE',
              name: 'RECIPIENT NAME (OPTIONAL)',
              type: 'to'
            }
          ],
          autotext: 'true',
          subject: 'YOUR SUBJECT HERE!',
          html: 'YOUR EMAIL CONTENT HERE! YOU CAN USE HTML!'
        }
      }
    }).done(function (response) {
      console.log(response) // if you're into that sorta thing
    })
  }
}
</script>
<style>
 @import "https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css";
</style>
