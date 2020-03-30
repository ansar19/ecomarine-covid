<template>
  <div id="app">
    <div class="сontainer mx-auto py-6 px-4">
      <form>
        <div class="w-4/5 mx-auto mt-4">
          <label
            class="block tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="infection-rate"
          >Коэффициент инфицирования, %</label>
          <input
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            v-model.number="infectionRate"
            id="infection-rate"
            type="text"
          />
          <p
            class="text-gray-600 text-xs italic"
          >Коэффициент инфицирования (распространенности) гриппа составляет 5-20%.</p>
          <p
            class="text-gray-600 text-xs italic"
          >Прогнозируется, что уровень заражения КОВИД-19 составит 40-70%.</p>
        </div>

        <div class="w-4/5 mx-auto mt-4">
          <label
            class="block tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-state"
          >Смертность среди возрастных групп, %</label>
          <div class="relative">
            <select
              class="block appearance-none w-full bg-gray-200 border border-gray-200 text-gray-700 py-3 px-4 pr-8 rounded leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
              v-model="selected"
              id="grid-state"
            >
              <option v-for="(item, index) in items" :key="index" v-bind:value="item">группа: "{{ item.ageGroup }}"</option>
            </select>
          </div>
          <p
            class="text-gray-600 text-xs italic"
          >Выбранная возрастная группа: {{ selected.ageGroup }}</p>
          <p
            class="text-gray-600 text-xs italic"
          >Численность населения в выбранной группе, человек: {{ selected.populationValue }}</p>
          <p
            class="text-gray-600 text-xs italic"
          >Коэффициент смертности в выбранной группе: {{ selected.mortalityRate }}</p>

          <!-- card container -->
          <div class="shadow-lg rounded overflow-hidden mt-2 sm:flex">
            <!-- card-content -->
            <div class="px-6 py-4">
              <h2 class="mb-2 text-gray-800">Справочная информация:</h2>
              <p
                class="text-orange-600 text-xs"
              >Источник по смертности среди возрастных групп: Adjusted age-specific case fatality ratio during the COVID-19 epidemic in Hubei, China, January and February 2020, medRxiv</p>
              <p
                class="text-orange-600 text-xs"
              >Источник по численности среди возрастных групп Казахстана: Демографический ежегодник Казахстана</p>
              <!--         https://stat.gov.kz/edition/publication/collection -->
              <p class="text-orange-600 text-xs">Смертность от гриппа составляет 0.1%.</p>
              <p
                class="text-orange-600 text-xs"
              >Данные из Южной Кореи, где правительство предприняло широко распространенные меры скрининга и инфекционного контроля, показывают, что смертность приближается к 0.8%.</p>
              <p
                class="text-orange-600 text-xs"
              >В настоящее время КОВИД-19 имеет тенденцию роста в мире на уровне 4.5%.</p>
            </div>
          </div>
        </div>
      </form>
    </div>

    <div
      id="wrapper"
      v-if="selected.ageGroup && selected.ageGroup.length"
      class="сontainer px-4 py-6 mx-auto"
    >
      <div class="w-4/5 mx-auto">
        <div class="flex flex-col sm:flex-row">
          <div
            class="sm:w-1/4 p-2 flex flex-col justify-center px-4 py-4 mt-2 mx-2 bg-white border border-gray-300 rounded sm:mt-0"
          >
            <div>
              <p class="text-2xl font-semibold text-center text-gray-800">{{infectedValue}}</p>
              <p
                class="text-md text-center text-gray-500"
              >Потенциальное число инфицированных, человек</p>
            </div>
          </div>

          <div
            class="flex flex-col justify-center px-4 py-4 mt-2 mx-2 bg-white border border-gray-300 rounded sm:mt-0"
          >
            <div>
              <p class="text-2xl font-semibold text-center text-gray-800">{{hospitalization}}</p>
              <p class="text-md text-center text-gray-500">Потенциальная потребность в койках</p>
              <p
                class="text-gray-500 text-center text-xs italic"
              >15% инфицированных необходимо будет госпитализировать.</p>
            </div>
          </div>

          <div
            class="flex flex-col justify-center px-4 py-4 mt-2 mx-2 bg-white border border-gray-300 rounded sm:mt-0"
          >
            <div>
              <p class="text-2xl font-semibold text-center text-gray-800">{{lungVentilator}}</p>
              <p
                class="text-md text-center text-gray-500"
              >Потенциально понадобится вентиляция легких, человек</p>
              <p
                class="text-gray-500 text-center text-xs italic"
              >5% инфицированных нуждаются в вентиляции легких.</p>
            </div>
          </div>

          <div
            class="flex flex-col justify-center px-4 py-4 mt-2 mx-2 bg-white border border-gray-300 rounded sm:mt-0"
          >
            <div>
              <p class="text-2xl font-semibold text-center text-gray-800">{{lethality}}</p>
              <p
                class="text-md text-center text-gray-500"
              >Летальность среди выбранной группы может составить, человек</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CovidCalc",
  data() {
    return {
      items: [
        {
          ageGroup: "Все возрастные группы",
          populationValue: 18395567,
          mortalityRate: 4.5
        },
        { ageGroup: "0-9 лет", populationValue: 3784254, mortalityRate: 0.01 },
        {
          ageGroup: "10-19 лет",
          populationValue: 2599477,
          mortalityRate: 0.02
        },
        {
          ageGroup: "20-29 лет",
          populationValue: 2759049,
          mortalityRate: 0.09
        },
        {
          ageGroup: "30-39 лет",
          populationValue: 2864184,
          mortalityRate: 0.18
        },
        { ageGroup: "40-49 лет", populationValue: 2244232, mortalityRate: 0.4 },
        { ageGroup: "50-59 лет", populationValue: 2002980, mortalityRate: 1.3 },
        { ageGroup: "60-69 лет", populationValue: 1321891, mortalityRate: 4.6 },
        { ageGroup: "70-79 лет", populationValue: 556751, mortalityRate: 9.8 },
        { ageGroup: "80 и выше", populationValue: 262749, mortalityRate: 18 }
      ],
      selected: "",
      infectionRate: 40
    };
  },
  computed: {
    infectedValue() {
      return (this.infectedValue = (
        this.selected.populationValue *
        this.infectionRate *
        0.01
      ).toFixed(0));
    },
    hospitalization() {
      return (this.hospitalization = (this.infectedValue * 0.15).toFixed(0));
    },
    lungVentilator() {
      return (this.lungVentilator = (this.infectedValue * 0.05).toFixed(0));
    },
    lethality() {
      return (this.lethality = (
        this.infectedValue *
        this.selected.mortalityRate *
        0.01
      ).toFixed(0));
    }
  }
};
</script>