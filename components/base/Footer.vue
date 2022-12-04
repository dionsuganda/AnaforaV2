<template>
  <footer class="relative">
    <div class="w-full h-[982px] bg-[url('~/assets/img/anafora/Footer.png')] bg-no-repeat">
      <!-- <div class="py-8 sm:py-4 text-center text-sm text-white hover:text-[#ffb236] h-full">
        &copy; Copyright 2022 ANAFORA. All rights reserved
      </div> -->
      <div class="grid grid-cols-12 h-full px-28">
        <div class="col-span-12 flex pt-[200px]">
          <div class="col-span-5 py-8 sm:py-4 text-center text-sm text-white hover:text-[#ffb236] self-end pt-[900px]">
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
          <div class="col-span-7 py-8 sm:py-4 text-sm text-white">
            <div class="pl-[120px] text-3xl font-bold pt-[100px]">
              OUR LOCATION
            </div>
            <div class="pl-[120px] pt-8 font-light">
              Jl. Inspeksi Kalimalang, Jembatan 2, Kp. Jati, RT. 004/RW. 002, Kel. Jatimulya, Kec. Tambun Selatan, Kabupaten Bekasi, Jawa Barat 17510
            </div>
          </div>
        </div>
        <div class="col-span-12 py-8 sm:py-4 text-center text-sm text-white hover:text-[#ffb236] self-end">
          <div class="pb-10 font-bold text-2xl">
            Curhat Yuk ? 0895 6152 15303 WhatsApp Chat Only
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
