<template>
  <div class="overflow-x-hidden">
    <Header />
    <div class="background--alt">
      <div class="container mx-auto flex md:min-h-screen">
        <div class="flex">
          <div class="inline-flex flex-col md:flex-row flex-no-wrap md:items-center">
            <div class="md:w-1/2 px-6 md:px-12 flex flex-col md:items-start">
              <h2
                class="mt-8 text-xl lg:text-3xl max-w-md leading-tight"
              >Первые случаи коронавирусной инфекции COVID-19 были зарегистрированы на территории Казахстана 13 марта 2020 года: два в Алма-Ате и один в Нур-Султане.</h2>
              <div
                class="mt-4 text-base lg:text-lg max-w-md open-sans-regular leading-snug"
              >15 марта президент Казахстана Касым-Жомарт Токаев подписал указ о введении в республике чрезвычайного положения на период с 8:00 16 марта 2020 года до 7:00 15 апреля 2020 года</div>
              <transition appear name="fade">
                <div class="inline-flex flex-row"></div>
              </transition>
            </div>
            <div class="md:w-1/2 md:px-16 mt-8 block md:hidden">
              <transition appear name="fade">
                <CovidStat />
              </transition>
            </div>
            <div class="md:w-1/2 md:px-16 hidden md:block">
              <transition appear name="fade">
                <CovidStat />
              </transition>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div id="map" class="flex">
      <div class="container mx-auto flex flex-col items-center mt-24 mb-24">
        <h1
          class="mt-16 text-center text-3xl md:text-4xl lg:text-5xl"
          v-scroll-reveal="{ delay: 500, distance: '15%' }"
        >Подтверждённые случаи по регионам Казахстана:</h1>
        <WikiInfo />
      </div>
    </div>
    <div id="precaution" class="flex px-8 md:px-0 background--alt">
      <div class="mx-auto flex flex-col flex-no-wrap items-center mt-24 mb-24">
        <h1
          class="text-2xl md:text-4xl text-center leading-tight"
        >Основные меры предосторожности для защиты от коронавирусной инфекции</h1>
        <p
          class="mt-4 text-center text-base md:text-xl lg:text-xl open-sans-regular leading-snug md:max-w-4xl md:px-32"
        >
          Следите за новейшей информацией о вспышке COVID-19, которую можно найти на веб-сайте ВОЗ и органов здравоохранения страны.
          В большинстве случаев заболевание характеризуется легким течением и заканчивается выздоровлением, хотя встречаются осложнения.
          Защитить свое здоровье и здоровье окружающих можно, соблюдая следующие правила:
        </p>
        <div class="mt-4 md:max-w-7xl flex flex-row items-center justify-around -mx-16 md:-mx-10">
          <Precaution />
        </div>
      </div>
    </div>
    <div id="myth" class="flex px-10 md:px-0">
      <div class="container mx-auto flex flex-col items-center mt-24 mb-24 md:mb-32">
        <h1 class="text-2xl md:text-4xl leading-tight">Мифы и ложные представления</h1>

        <div class="w-5/6 md:w-3/4 mt-3">
          <Myth />
        </div>

      </div>
    </div>

    <Footer />
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import CovidStat from "@/components/CovidStat.vue";
import WikiInfo from "@/components/WikiInfo.vue";
import Precaution from "@/components/Precaution.vue";
import Myth from "@/components/Myth.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "Home",
  components: {
    Header,
    CovidStat,
    WikiInfo,
    Precaution,
    Myth,
    Footer
  }
};
</script>



