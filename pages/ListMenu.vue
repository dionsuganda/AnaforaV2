<template>
  <div class="w-full bg-[#22272B]">
    <nav id="navbar" class="relative z-10 w-full">
    <div class="flex flex-col max-w-screen-xl px-8 mx-auto lg:items-center lg:justify-between">
      <div class="w-10/12 flex flex-col lg:flex-row items-center space-x-4 xl:space-x-8">
        <div class="w-full flex flex-row items-center justify-between py-4">
          <div>
            <img :src="require('~/assets/img/anafora/Logo.svg')" class="w-24 xl:w-28 ml-2" alt="Nefa Logo" />
          </div>
          <button class="rounded-lg lg:hidden focus:outline-none focus:shadow-outline" @click="open = !open">
            <SegmentIcon v-if="!open" :size="24" />
            <CloseIcon v-else :size="24" />
          </button>
        </div>
        <ul
          :class="[open ? 'flex' : 'hidden lg:flex']"
          class="w-full h-auto flex flex-col flex-grow lg:items-center pb-4 lg:pb-0 lg:justify-end lg:flex-row origin-top duration-300 xl:space-x-2 space-y-3 lg:space-y-0"
        >
            <li class="w-full">
              <a
                class="md:px-4 py-2 text-base font-semibold bg-transparent rounded-lg text-[#E7D191] hover:text-gray-900 focus:outline-none focus:shadow-outline"
                href="ListMenu"
              >
                Promo
              </a>
            </li>
            <li class="w-full">
              <a
                class="md:px-4 py-2 text-base font-semibold bg-transparent rounded-lg text-[#E7D191] hover:text-gray-900 focus:outline-none focus:shadow-outline"
                href="ListMenu"
              >
                List Menu
              </a>
            </li>
            <li class="w-full">
              <a
                class="md:px-4 py-2 text-base font-semibold bg-transparent rounded-lg text-[#E7D191] hover:text-gray-900 focus:outline-none focus:shadow-outline"
                href="ListMenu"
              >
                Contact
              </a>
            </li>
            <li class="w-full">
              <a
                class="md:px-4 py-2 text-base font-semibold bg-transparent rounded-lg text-[#E7D191] hover:text-gray-900 focus:outline-none focus:shadow-outline"
                href="ListMenu"
              >
                About
              </a>
            </li>
        </ul>
      </div>
    </div>
  </nav>
    <!-- Hero section -->
    <section id="hero" class="w-full pb-24">
      <div class="block md:hidden justify-self-center mx-10">
        <img
          data-aos="fade-up"
          data-aos-once="true"
          :src="require('~/assets/img/anafora/Transparent-Product.svg')"
          class="mt-4"
          width="500"
          alt=""
        />
      </div>
      <div class="grid grid-cols-12 gap-4 mt-0 lg:mt-16">
        <div class="col-span-12 lg:col-span-6 justify-self-center m-5 pl-0 lg:pl-36 pt-8">
          <h2 data-aos="fade-down" data-aos-once="true" data-aos-delay="300" class="font-semibold mb-8 lg:mb-8">
            <p class="text-4xl lg:text-7xl font-bold font-sans text-center lg:text-left text-[#E7D191]">
              WE SERVE THE TASTE YOU LOVE!
            </p>
          </h2>
          <p data-aos="fade-down" data-aos-once="true" data-aos-delay="300" class="sm:block text-1xl font-sans font-light text-center lg:text-left text-white">
            This is type of cafe which typically serve food and drink. In addition to light refreshment such as baked goods or snacks. The term come from the rench word meaning food.
          </p>
        </div>
        <div class="invisible lg:visible lg:col-span-6 lg:justify-self-center">
          <img
            data-aos="fade-up"
            data-aos-once="true"
            :src="require('~/assets/img/anafora/Transparent-Product.svg')"
            class="mt-4"
            width="500"
            alt=""
          />
        </div>
      </div>
      <div v-for="(menus, index) in menu" :key="index" class="mx-5 lg:mx-24">
        <div v-for="iteration in menus.drinks.length" :key="iteration">
          <h2 data-aos="fade-down" data-aos-once="true" data-aos-delay="300" class="font-semibold my-8">
            <p class="text-4xl lg:text-7xl font-bold font-sans text-center text-[#E7D191]">
              {{ menus.drinks[iteration -1].type}}
              <!-- {{ iteration }} -->
            </p>
          </h2>
          <div class="flex flex-wrap justify-center lg:justify-start gap-4 lg:m-5">
            <div v-for="iteration2 in menus.drinks[iteration -1].menu.length" :key="iteration2" class="justify-self-center self-center basis-36 lg:basis-72 bg-gradient-to-br from-[#24252b] to-[#2F3336] rounded-lg drop-shadow-2xl h-72 lg:h-auto">
              <img
                data-aos="fade-up"
                data-aos-once="true"
                :src="require('~/assets/img/anafora/product/red-velvet.svg')"
                class="mt-4 object-contain max-h-40 w-80"
                alt=""
              />
              <div class="pl-3 pr-3">
                <span data-aos="fade-down" data-aos-once="true" data-aos-delay="300" class="sm:block text-sm lg:text-xl text-center text-[#E7D191] font-bold font-['Poppins'] tracking-widest" width="643">
                  {{ menus.drinks[iteration-1].menu[iteration2-1].name}}
                </span>
              </div>
              <div class="pl-3 pr-3 pb-3">
                <span data-aos="fade-down" data-aos-once="true" data-aos-delay="300" class="sm:block text-sm lg:text-1xl text-center text-white font-semibold font-['Poppins'] tracking-widest pb-5" width="643">
                  Rp. {{ menus.drinks[iteration-1].menu[iteration2-1].price.ice}}
                </span>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div v-for="(menus, index) in menu" :key="index" class="mx-5 lg:mx-24">
        <div v-for="iteration in menus.food.length" :key="iteration">
          <h2 data-aos="fade-down" data-aos-once="true" data-aos-delay="300" class="font-semibold my-8">
            <p class="text-4xl lg:text-7xl font-bold font-sans text-center text-[#E7D191]">
              {{ menus.food[iteration -1].type}}
              <!-- {{ iteration }} -->
            </p>
          </h2>
          <div class="flex flex-wrap justify-center lg:justify-start gap-4 lg:m-5">
            <div v-for="iteration2 in menus.food[iteration -1].menu.length" :key="iteration2" class="justify-self-center self-center basis-36 lg:basis-72 bg-gradient-to-br from-[#24252b] to-[#2F3336] rounded-lg drop-shadow-2xl h-72 lg:h-auto">
              <div v-if="menus.food[iteration-1].menu[iteration2-1].photoUrl != ''" class="flex justify-center">
                <img
                  data-aos="fade-up"
                  data-aos-once="true"
                  :src="require('~/assets/img/anafora/product/' + menus.food[iteration-1].menu[iteration2-1].photoUrl)"
                  class="m-4 object-contain max-h-40 w-28 lg:max-w-64 rounded-lg"
                  alt=""
                />
              </div>
              <div v-else class="">
                <img
                  data-aos="fade-up"
                  data-aos-once="true"
                  :src="require('~/assets/img/anafora/product/red-velvet.svg')"
                  class="mt-4 object-contain max-h-40 w-80"
                  alt=""
                />
              </div>

              <div class="pl-3 pr-3">
                <span data-aos="fade-down" data-aos-once="true" data-aos-delay="300" class="sm:block text-sm lg:text-xl text-center text-[#E7D191] font-bold font-['Poppins'] tracking-widest" width="643">
                  {{ menus.food[iteration-1].menu[iteration2-1].name}}
                </span>
              </div>
              <div class="pl-3 pr-3 pb-3">
                <span data-aos="fade-down" data-aos-once="true" data-aos-delay="300" class="sm:block text-sm lg:text-1xl text-center text-white font-semibold font-['Poppins'] tracking-widest pb-5" width="643">
                  Rp. {{ menus.food[iteration-1].menu[iteration2-1].price}}
                </span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>


    <!-- Credit card section -->
    <!-- <section class="w-full my-36 mt-[300px]">
      <BaseSection data-aos="fade-down">
        <div class="col-span-12 lg:col-span-4 space-y-6 px-4 sm:px-6 mt-4">
          <h2 class="text-3xl lg:text-4xl font-semibold text-center mb-8 lg:mb-0">
            <span class="text-header-gradient">MONTHLY PROMO!</span>
          </h2>
        </div>
        <div class="col-span-12 lg:col-span-4 mt-2 lg:mt-0">
          <div class="w-full">
            <img :src="require('~/assets/img/anafora/Promo1.png')" class="w-[391px] h-[314px] drop-shadow-xl" alt="" />
          </div>
          <div class="mt-4 space-y-6 px-4 col-span-12 lg:col-span-5 text-center">
            <h1 class="text-2xl font-['Abel'] mt-7 first-letter:mt-10 drop-shadow-lg">
              KOPI SUSU GULA AREN
            </h1>
            <p class="mt-10 drop-shadow-lg">
              Get a discount of 30%, maximum 30K.
            </p>
          </div>
        </div>
        <div class="col-span-12 lg:col-span-4 mt-2 lg:mt-0">
          <div class="w-full">
            <img :src="require('~/assets/img/anafora/Promo2.png')" class="w-[391px] h-[314px] drop-shadow-xl" alt="" />
          </div>
          <div class="mt-4 space-y-6 px-4 col-span-12 lg:col-span-5 text-center">
            <h1 class="text-2xl font-['Abel'] mt-7 first-letter:mt-10 drop-shadow-lg">
              CARAMEL LATTE
            </h1>
            <p class="mt-10 drop-shadow-lg">
              Get a discount of 30%, maximum 30K.
            </p>
          </div>
        </div>
      </BaseSection>
    </section> -->

    <div class="w-full mt-10 flex justify-center">
      <a
        v-smooth-scroll
        data-aos="flip-down"
        data-aos-delay="150"
        href="#navbar"
        class="px-6 py-3 flex items-center space-x-2 bg-[#FAFAFA] hover:bg-gray-100 hover:shadow-md border border-[#DDDDDD] rounded-md text-gray-700"
      >
        <span>Back to top</span>
        <ArrowUpIcon :size="20" />
      </a>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import aosMixin from '@/mixins/aos'
// import json from '~/assets/json/list-menu.json'
export default {
  name: 'IndexPage',
  mixins: [aosMixin],
  data() {
    return {
      // menu: json,
      menu: null,
      open: false,
      dropdownNavbar: false,
      selected: 0,
      dropdownConcurency: false,
      dropdownCrypto: false,
      currencySelected: {
        img: 'country-icon/eng.png',
        name: 'USD',
      },
      currencies: [
        {
          img: 'country-icon/eng.png',
          name: 'USD',
        },
      ],
      cryptoSelected: {
        img: 'crypto-icon/bitcoin.png',
        name: 'BTC',
      },
      cryptocurrencies: [
        {
          img: 'crypto-icon/bitcoin.png',
          name: 'BTC',
        },
      ],
      trendings: [
        {
          id: 1,
          name: 'Bitcoin',
          price: 43180.13,
          logo: 'bitcoin.png',
          increase: true,
          data: [40, 35, 60, 75, 60, 75, 50],
        },
        {
          id: 2,
          name: 'Ethereum',
          price: 3480.65,
          logo: 'ethereum.png',
          increase: false,
          data: [25, 30, 60, 50, 80, 55, 80],
        },
        {
          id: 3,
          name: 'Solana',
          price: 150.2,
          logo: 'solana.png',
          increase: true,
          data: [40, 45, 40, 80, 50, 60, 35],
        },
        {
          id: 4,
          name: 'Dogecoin',
          price: 0.1572,
          logo: 'dogecoin.png',
          increase: true,
          data: [35, 70, 60, 80, 50, 60, 40],
        },
      ],
      topGainers: [
        {
          id: 1,
          name: 'PAPPAY',
          price: 0.00374,
          logo: 'pappay.png',
          increase: true,
          data: [30, 50, 45, 60, 70, 40, 45],
        },
        {
          id: 2,
          name: 'Bitcoin Asia',
          price: 0.02096,
          logo: 'bitcoin-asia.png',
          increase: true,
          data: [25, 60, 50, 60, 35, 50, 70],
        },
        {
          id: 3,
          name: 'MoonRock',
          price: 0.004907,
          logo: 'moonrock.png',
          increase: true,
          data: [40, 35, 40, 25, 50, 70, 45],
        },
        {
          id: 4,
          name: 'NinjaFloki',
          price: 0.000123,
          logo: 'ninjafloki.png',
          increase: true,
          data: [45, 35, 40, 30, 25, 45, 35],
        },
      ],
      recents: [
        {
          id: 1,
          name: 'MetaCraft',
          price: 0.0608,
          logo: 'metacraft.png',
          increase: false,
          data: [40, 50, 45, 60, 35, 40, 45],
        },
        {
          id: 2,
          name: 'Frog',
          price: 0.5875,
          logo: 'frog.png',
          increase: false,
          data: [25, 50, 45, 48, 40, 60, 45],
        },
        {
          id: 3,
          name: 'Musk Doge',
          price: 0.04041,
          logo: 'musk-doge.png',
          increase: true,
          data: [25, 35, 60, 45, 50, 45, 45],
        },
        {
          id: 4,
          name: '2SHARE',
          price: 1366.24,
          logo: '2share.png',
          increase: true,
          data: [35, 30, 60, 50, 35, 45, 40],
        },
      ],
      accordions: [
        {
          title: 'Why should I choose NEFA?',
          description:
            "We're industry pioneers, having been in the cryptocurrency industry since 2016. We've facilitated more than 21 billion USD worth of transactions on our exchange for customers in over 40 countries. Today, we're trusted by over 8 million customers around the world and have received praise for our easy-to-use app, secure wallet, and range of features.",
        },
        {
          title: 'How secure is NEFA?',
          description:
            "We're industry pioneers, having been in the cryptocurrency industry since 2016. We've facilitated more than 21 billion USD worth of transactions on our exchange for customers in over 40 countries. Today, we're trusted by over million customers around the world and have received praise for our easy-to-use app, secure wallet, and range of features.",
        },
        {
          title: 'Do I have to buy a whole Bitcoin?',
          description:
            "We're industry pioneers, having been in the cryptocurrency industry since 2016. We've facilitated more than 21 billion USD worth of transactions on our exchange for customers in over 40 countries. Today, we're trusted by over million customers around the world and have received praise for our easy-to-use app, secure wallet, and range of features.",
        },
        {
          title: 'How do I actually buy Bitcoin?',
          description:
            "We're industry pioneers, having been in the cryptocurrency industry since 2016. We've facilitated more than 21 billion USD worth of transactions on our exchange for customers in over 40 countries. Today, we're trusted by over million customers around the world and have received praise for our easy-to-use app, secure wallet, and range of features.",
        },
      ],
      steps: [
        {
          img: 'sign-up.png',
          title: 'Sign Up',
          description:
            'Sign up for your free NEFA Wallet on web, iOS or Android and follow our easy process to set up your profile',
        },
        {
          img: 'fund.png',
          title: 'Fund',
          description:
            'Choose your preferred payment method such as bank transfer or credit card to top up your NEFA Wallet',
        },
        {
          img: 'buy-crypto.png',
          title: 'Buy Crypto',
          description:
            'Buy Bitcoin or Ethereum, then securely store it in your Wallet or send it on easily to your friends anywhere',
        },
      ],
    }
  },
  // async created() {
  //   try {
  //     const res = await axios.get(`https://menu.anafora.id/list-menu.json`);
  //     this.menu = res.data;
  //   } catch (error) {
  //     // console.log(error);
  //   }
  // },
  mounted () {
    axios
      .get('https://menu.anafora.id')
      .then(response => (this.menu = response.data))
  },
  methods: {
    dropdownToggler () {
      this.dropdownNavbar = !this.dropdownNavbar
    }
  }
}
</script>
<style scoped>
.text-header-gradient {
  background: rgb(57, 132, 244);
  background: linear-gradient(169.4deg, #0a4217 -6.01%,#44cd76 36.87%,#116530 78.04%,#0B4619 103.77%);
  background-clip: text;
  -webkit-text-fill-color: transparent;
}
.bg-partner {
  background: url('../assets/img/partner/background.png');
  background-size: cover;
  background-position: center;
}
.bg-trading-tools {
  background: url('../assets/img/bg-trading-tools.webp');
  background-size: cover;
  background-position: center;
}
.max-h-0 {
  max-height: 0;
}
</style>
