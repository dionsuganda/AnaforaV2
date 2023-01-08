<template>
  <div class="w-full">
    <BaseNavbar />
    <div
        class="absolute top-0 left-0 w-full h-[125vh] sm:h-[225vh] lg:h-[125vh] bg-[url('~/assets/img/anafora/Background.png')] bg-no-repeat sm:cover-gradient"
      ></div>
    <!-- Hero section -->
    <section id="hero" class="w-full pb-24">
      <BaseSection>
        <div class="grid grid-cols-12 col-span-12 mt-12 xl:mt-10 space-y-4 sm:space-y-6 px-6 text-center sm:text-left">
          <div class="sm:block col-span-12">
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
          <div class="col-span-12 pt-8 xl:col-span-7 xl:pt-0">
            <span data-aos="fade-down" data-aos-once="true" data-aos-delay="300" class="sm:block text-2xl text-white font-light font-['Poppins'] tracking-widest pr-5" width="643">
              The most appropriate place to recover your mood at Anafora Coffee, Come on! And restore your happy mood right now!
            </span>
          </div>
        </div>
      </BaseSection>
    </section>

    <!-- Crypto statistic section -->

    <!-- Buy and trade section -->
    <section class="w-full my-24 mt-96">
      <BaseSection>
        <!-- <div class="flex col-span-12"> -->
          <!-- <LandingBuyTradeImage class="sm:hidden mb-8" /> -->
          <LandingBuyTradeImage data-aos="fade-right" class="sm:block col-span-12 lg:col-span-7" />
          <div data-aos="fade-left" class="h-full lg:h-64 mt-4 xl:mt-96 mb-10 space-y-6 px-4 col-span-12 lg:col-span-5 bg-[#E8E8CC] lg:-ml-28 text-center text-2xl drop-shadow-xl">
            <p class="paragraph mt-10">
              We have a dream to serve quality coffee, made with fresh ingredients to customers all over Indonesia.
            </p>
            <p class="paragraph">
              - Anafora -
            </p>
          </div>
        <!-- </div> -->
      </BaseSection>
    </section>

    <!-- Partners section -->
    <!-- <section class="bg-partner relative max-w-full sm:mx-6 my-24 shadow sm:rounded-2xl overflow-hidden">
      <div class="w-full px-6 sm:px-0 py-16 flex flex-col items-center justify-center space-y-4 text-center">
        <h3 data-aos="flip-down" class="text-2xl text-neutral-800 font-semibold">Trusted Partners Worldwide</h3>
        <p data-aos="flip-down" class="paragraph">We're partners with countless major organisations around the globe</p>
        <div data-aos="fade-up" class="flex flex-wrap items-center justify-center">
          <LandingPartnerImage
            v-for="img in ['clever.png', 'diamon-cutts.png', 'swiss-finance.png', 'gambio.png']"
            :key="img"
            :img="img"
          />
        </div>
      </div>
    </section> -->

    <!-- Credit card section -->
    <section class="w-full my-36 mt-[300px]">
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
    </section>

    <div class="w-full my-10 flex justify-center">
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
import aosMixin from '@/mixins/aos'
export default {
  name: 'IndexPage',
  mixins: [aosMixin],
  data() {
    return {
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
