<template>
  <div id="app">
    <div
      class="mt-4 mx-4 text-base lg:text-lg open-sans-regular leading-snug"
    >Для того чтобы оценить масштабы пандемии, ниже представлен калькулятор по расчету: потенциальных заболевших, необходимости койко-мест, аппаратов искуственной вентиляции легких и летальности среди различных возрастных групп.</div>
    <div class="сontainer mx-auto py-6 px-4">
      <form>
        <div class="w-4/5 mx-auto mt-4">
          <label
            class="block tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="infection-rate"
          >Коэффициент инфицирования, %</label>
          <input
            class="focus:underline appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            v-model.number="infectionRate"
            id="infection-rate"
            type="text"
          />
          <p
            class="text-gray-600 text-xs italic"
          >Коэффициент инфицирования (распространенности) гриппа составляет 5-20%.</p>
          <p
            class="text-gray-600 text-xs italic"
          >Прогнозируется, что уровень заражения COVID-19 составит 40-70%.</p>
        </div>

        <div class="w-4/5 mx-auto mt-4">
          <div class="w-full">
            <label
              class="block tracking-wide text-gray-700 text-xs font-bold mb-2"
              for="grid-state"
            >Выберите возрастную группу</label>
            <svg
              version="1.1"
              id="Capa_1"
              xmlns="http://www.w3.org/2000/svg"
              xmlns:xlink="http://www.w3.org/1999/xlink"
              x="0px"
              y="0px"
              width="20px"
              height="20px"
              viewBox="0 0 93.43 93.43"
              style="enable-background:new 0 0 93.43 93.43;"
              xml:space="preserve"
            >
              <g>
                <g>
                  <path
                    d="M38.764,93.43c1.814,0,3.484-0.597,4.844-1.597c0,0,3.304-2.55,3.304-5.32c0-1.598,0.029-14.684,0.045-22.063
			c4.367,2.806,9.564,1.613,11.318,1.076c1.875-0.377,3.03-0.299,5.394-0.53c2.767-0.357,6.013-1.816,9.012-4.741
			c0.608-0.438,1.675-0.674,2.804-0.919c3.043-0.66,7.64-1.661,8.926-8.506l0.022-0.163c0.05-0.559,1.196-13.787-1.604-21.409
			c-1.045-2.85-1.988-4.479-2.745-5.79c-0.599-1.035-1.073-1.875-1.429-3.08c2.547-0.25,4.549-2.379,4.549-4.99V5.04
			c0-2.779-2.26-5.04-5.038-5.04H31.223c-2.779,0-5.039,2.261-5.039,5.04v10.358c0,2.755,2.223,4.994,4.969,5.032
			c-0.843,3.996-4.137,9.353-14.337,14.086c-0.981,0.346-8.092,3.059-8.093,9.105c0,0.155,0.039,3.813,3.327,5.738
			c3.709,2.172,9.802,1.039,18.129-3.365c0.203,0.769,0.383,1.869,0.383,3.33v35.904C30.563,89.751,34.242,93.43,38.764,93.43z
			 M31.783,14.839v-9.24h45.821v9.239L31.783,14.839L31.783,14.839z"
                  />
                  <circle cx="37.477" cy="10.226" r="3.266" />
                </g>
              </g>
              <g />
              <g />
              <g />
              <g />
              <g />
              <g />
              <g />
              <g />
              <g />
              <g />
              <g />
              <g />
              <g />
              <g />
              <g />
            </svg>
            <div class="relative mt-1">
              <select
                v-model="selected"
                class="block appearance-none w-full bg-gray-200 border border-gray-200 text-gray-700 py-3 px-4 pr-8 rounded leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
                id="grid-state"
              >
                <option
                  v-for="(item, index) in items"
                  :key="index"
                  v-bind:value="item"
                >группа: "{{ item.ageGroup }}"</option>
              </select>
              <div
                class="pointer-events-none absolute inset-y-0 right-0 flex items-center px-2 text-gray-700"
              >
                <svg
                  class="fill-current h-4 w-4"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 20 20"
                >
                  <path
                    d="M9.293 12.95l.707.707L15.657 8l-1.414-1.414L10 10.828 5.757 6.586 4.343 8z"
                  />
                </svg>
              </div>
            </div>
          </div>

          <div
            class="background--alt border-t border-b border-blue-500 text-blue-700 mt-2 px-4 py-3"
            role="alert"
          >
            <p class="text-sm">Выбранная возрастная группа: {{ selected.ageGroup }}</p>
            <p
              class="text-sm"
            >Численность населения в выбранной группе, человек: {{ selected.populationValue }}</p>
            <p
              class="text-sm"
            >Коэффициент смертности в выбранной группе: {{ selected.mortalityRate }}</p>
          </div>

          <!-- card container -->
          <div class="shadow-lg rounded overflow-hidden mt-2 sm:flex">
            <!-- card-content -->
            <div class="px-6 py-4">
              <h2 class="mb-2 text-gray-800">Справочная информация:</h2>
              <p class="text-orange-600 text-xs">
                Источник по смертности среди возрастных групп:
                <a
                  class="link open-sans-regular text-grey-darker hover-link"
                  href="https://www.medrxiv.org/content/10.1101/2020.03.04.20031104v1.full.pdf"
                  target="_blank"
                  rel="noopener noreferrer"
                >Adjusted age-specific case fatality ratio during the COVID-19 epidemic in Hubei, China, January and February 2020, medRxiv</a>
              </p>
              <p class="text-orange-600 text-xs">
                Источник по численности среди возрастных групп Казахстана:
                <a
                  class="link open-sans-regular text-grey-darker hover-link"
                  href="https://stat.gov.kz/edition/publication/collection"
                  target="_blank"
                  rel="noopener noreferrer"
                >Демографический ежегодник Казахстана</a>
              </p>
              <p class="text-orange-600 text-xs">Смертность от гриппа составляет 0.1%.</p>
              <p
                class="text-orange-600 text-xs"
              >Данные из Южной Кореи, где правительство предприняло широко распространенные меры скрининга и инфекционного контроля, показывают, что смертность приближается к 0.8%.</p>
              <p class="text-orange-600 text-xs">
                В настоящее время летальность от
                <a
                  class="link open-sans-regular text-grey-darker hover-link"
                  href="https://www.who.int/dg/speeches/detail/who-director-general-s-opening-remarks-at-the-media-briefing-on-covid-19---3-march-2020"
                  target="_blank"
                  rel="noopener noreferrer"
                >COVID-19 находится на уровне 3.4%</a>
                .
              </p>
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
            class="shadow-lg sm:w-1/4 p-2 flex flex-col justify-center px-4 py-4 mt-2 mx-2 bg-white border border-gray-300 rounded sm:mt-0"
          >
            <div>
              <p class="text-2xl font-semibold text-center text-gray-800">{{infectedValue}}</p>
              <p
                class="text-md text-center text-gray-500"
              >Потенциальное число инфицированных, человек</p>
            </div>
          </div>

          <div
            class="shadow-lg flex flex-col justify-center px-4 py-4 mt-2 mx-2 bg-white border border-gray-300 rounded sm:mt-0"
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
            class="shadow-lg flex flex-col justify-center px-4 py-4 mt-2 mx-2 bg-white border border-gray-300 rounded sm:mt-0"
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
            class="shadow-lg flex flex-col justify-center px-4 py-4 mt-2 mx-2 bg-white border border-gray-300 rounded sm:mt-0"
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
          mortalityRate: 3.4
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