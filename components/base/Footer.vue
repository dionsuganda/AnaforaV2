<template>
  <footer class="w-full h-full">
    <div class="w-full lg:h-[982px] bg-[url('~/assets/img/anafora/Footer.png')] bg-no-repeat">
      <!-- <div class="py-8 sm:py-4 text-center text-sm text-white hover:text-[#ffb236] h-full">
        &copy; Copyright 2022 ANAFORA. All rights reserved
      </div> -->
      <div class="grid grid-cols-12 h-full px-4 lg:px-28">
        <div class="col-span-12 lg:flex lg:pt-[90px]">
          <div class="col-span-12 lg:py-8 sm:py-4 text-center text-sm text-white hover:text-[#ffb236] self-end">
            <div class="w-full">
                <img
                  data-aos="fade-up"
                  data-aos-once="true"
                  :src="require('~/assets/img/anafora/Logo.svg')"
                  class="mt-4"
                  width="500"
                  alt=""
                />
              </div>
          </div>
          <div class="col-span-12 lg:py-8 sm:py-4 text-sm text-white lg:pl-[120px] text-center lg:text-left">
            <div class="text-3xl font-bold pt-4 lg:pt-[100px]">
              OUR LOCATION
            </div>
            <a class="hover:text-[#ffb236]" href="https://goo.gl/maps/1mdSR4QKa7wyvRZK9">
              <div class="pt-8 pb-4 lg:0 font-light">
                Jl. Inspeksi Kalimalang, Jembatan 2, Kp. Jati, RT. 004/RW. 002, Kel. Jatimulya, Kec. Tambun Selatan, Kabupaten Bekasi, Jawa Barat 17510
              </div>
              <img
                    data-aos="fade-up"
                    data-aos-once="true"
                    :src="require('~/assets/img/anafora/anaforamaps.jpeg')"
                    class="mb-4 lg:mb-0 lg:mt-4 w-full h-[300px]"
                    alt=""
                  />
            </a>
          </div>
        </div>
        <div class="col-span-12 lg:py-8 lg:mt-[60px] sm:py-4 text-center text-sm text-white self-end">
          <div class="pb-10 font-bold text-2xl">
            Curhat Yuk ? 0895-2995-5553 WhatsApp Chat Only
          </div>
          <div class="pb-10 text-thin">
            Consumer Complaints Service Contact Information
          </div>
          &copy; Copyright 2022 ANAFORA. All rights reserved
        </div>
      </div>
    </div>
  </footer>
</template>
<script>
export default {
  name: 'BaseFooter',
}
</script>
