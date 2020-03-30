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
              >Первые случаи коронавирусной инфекции COVID-19 были зарегистрированы на территории Казахстана 13 марта 2020 года: два в Алматы и один в Нур-Султане.</h2>
              <div
                class="mt-4 text-base lg:text-lg max-w-md open-sans-regular leading-snug"
              >15 марта президент Казахстана подписал указ о введении в республике чрезвычайного положения на период с 8:00 16 марта 2020 года до 7:00 15 апреля 2020 года</div>
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

    <div id="covid-calc" class="flex">
      <div class="container mx-auto flex flex-col items-center mt-24 mb-24">
        <!--  mt-16 text-center text-3xl md:text-4xl lg:text-5xl-->
        <h1
          class="text-2xl md:text-4xl text-center leading-tight"
          v-scroll-reveal="{ delay: 500, distance: '15%' }"
        >Калькулятор COVID-19 по Казахстану</h1>
        <CovidCalc />
      </div>
    </div>

    <div id="chronology" class="flex px-8 md:px-0 background--alt">
      <div class="mx-auto flex flex-col flex-no-wrap items-center mt-24 mb-24">
        <h1
          class="text-2xl md:text-4xl text-center leading-tight"
        >Хронология проявления симптомов короновируса</h1>
        <p
          class="mt-4 text-center text-base md:text-xl lg:text-xl open-sans-regular leading-snug md:max-w-4xl md:px-32"
        >
          На начальном этапе заражения новый коронавирус активно размножается в горле и верхних дыхательных путях. Потом инфекция опускается ниже и может добраться до легких, вызывая воспаление.
<p
          class="mt-4 text-center text-base md:text-xl lg:text-xl open-sans-regular leading-snug md:max-w-4xl md:px-32"
        >Именно поэтому первый симптом заражения - кашель. Уже потом начинает повышаться температура. </p>
<p
          class="mt-4 text-center text-base md:text-xl lg:text-xl open-sans-regular leading-snug md:max-w-4xl md:px-32"
        >Но у 30% пациентов в Ухане температура на момент прибытия в больницу была не выше нормы.</p>
<p
          class="mt-4 text-center text-base md:text-xl lg:text-xl open-sans-regular leading-snug md:max-w-4xl md:px-32"
        >У многих заразившихся (18% или почти каждого пятого) нет даже кашля. Болезнь протекает вообще без симптомов - человек может даже не подозревать, что болен.
При этом такой бессимптомный больной всё равно является активным носителем инфекции и может заражать других.
        </p>
        <div class="mt-4 md:max-w-7xl flex flex-row items-center justify-around -mx-16 md:-mx-10">
          <CovidTimeLine />
        </div>
      </div>
    </div>


<div id="body" class="flex">
      <div
        class="container mx-auto flex flex-col items-center mt-24 mb-24 md:mb-32"
      >
        <div
          class="md:mt-16 inline-flex flex-col-reverse lg:flex-row px-6 md:px-0 flex-no-wrap items-center justify-center"
        >
          <div
            class="md:w-1/2 flex flex-col md:max-w-lg md:items-start md:pl-6 md:pr-8"
          >
            <h1
              class="mt-16 text-center md:text-left lg:mt-0 text-2xl md:text-4xl gt-walsheim-medium leading-tight"
            >
              Каковы симптомы COVID‑19?
            </h1>
            <h2
              class="mt-4 text-center md:text-left text-xl md:text-2xl gt-walsheim-regular leading-tight px-6 md:px-0"
            >
              К наиболее распространенным симптомам COVID‑19 относятся повышение температуры тела, утомляемость и сухой кашель. 
            </h2>
            <div
              class="mt-4 text-center md:text-left text-base md:text-base lg:text-lg open-sans-regular leading-normal"
            >
              У ряда пациентов могут отмечаться различные боли, заложенность носа, насморк, фарингит или диарея. Как правило, эти симптомы развиваются постепенно и носят слабо выраженный характер. У некоторых инфицированных лиц не возникает каких-либо симптомов или плохого самочувствия. У большинства людей (порядка 80%) болезнь заканчивается выздоровлением, при этом специфических лечебных мероприятий не требуется. Примерно в одном из шести случаев COVID-19 возникает тяжелая симптоматика с развитием дыхательной недостаточности. У пожилых людей, а также лиц с имеющимися соматическими заболеваниями, например, артериальной гипертензией, заболеваниями сердца или диабетом, вероятность тяжелого течения заболевания выше. При наличии повышенной температуры тела, кашля и затрудненного дыхания следует обращаться за медицинской помощью.
            </div>
          </div>
          <!-- right side -->
          <div
            class="md:w-1/2 max-w-5xl px-20 md:px-20"
            v-scroll-reveal="{ delay: 1000, distance: '20%' }"
          >
            <Body />
          </div>
          <!-- END right side -->
        </div>
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

        <div class="w-11/12 md:w-3/4 mt-3">
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
import CovidCalc from "@/components/CovidCalc.vue";
import CovidTimeLine from "@/components/CovidTimeLine.vue";
import Body from "@/components/Body.vue";
import WikiInfo from "@/components/WikiInfo.vue";
import Precaution from "@/components/Precaution.vue";
import Myth from "@/components/Myth.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "Home",
  components: {
    Header,
    CovidStat,
    CovidCalc,
    CovidTimeLine,
    Body,
    WikiInfo,
    Precaution,
    Myth,
    Footer
  }
};
</script>



