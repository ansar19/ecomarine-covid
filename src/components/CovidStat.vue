<template>
  <div class="container mx-4 ">
    <h1 class="mb-8 ml-4">Данные по COVID-19 в Казахстане на: {{ lastUpdate | human_readable }}</h1>
    <table
      class="w-full ml-2 flex flex-row flex-no-wrap sm:bg-white rounded-lg overflow-hidden sm:shadow-lg my-5"
    >
      <thead class="text-grey">
        <tr
          class="bg-400 flex flex-col flex-no wrap sm:table-row rounded-l-lg sm:rounded-none mb-2 sm:ml-2"
        >
          <th class="p-3 text-left">Подтвержденных случаев</th>
          <th class="p-3 text-left">Новых случаев</th>
          <th class="p-3 text-left">Смертей</th>
          <th class="p-3 text-left">Излечились</th>
        </tr>
      </thead>
      <tbody class="flex-1 sm:flex-none">
        <tr
          v-for="(info, index) in filteredList"
          :key="index"
          class="flex flex-col flex-no wrap sm:table-row mb-2 sm:ml-2"
        >
          <td
            class="border-grey-light border hover:bg-gray-100 p-3 truncate"
          >{{info.TotalConfirmed}}</td>
          <td class="border-grey-light border hover:bg-gray-100 p-3 truncate">
            {{info.NewConfirmed}}
            ({{(info.NewConfirmed/info.TotalConfirmed*100).toFixed(2)}}%)
          </td>
          <td class="border-grey-light border hover:bg-gray-100 p-3 truncate">
            {{info.TotalDeaths}}
            ({{(info.TotalDeaths/info.TotalConfirmed*100).toFixed(2)}}%)
          </td>
          <td class="border-grey-light border hover:bg-gray-100 p-3 truncate">
            {{info.TotalRecovered}}
            ({{(info.TotalRecovered/info.TotalConfirmed*100).toFixed(2)}}%)
          </td>
        </tr>
      </tbody>
    </table>
    <p
            class="text-gray-600 text-xs italic">Источник: 
            <a
                class="link open-sans-regular text-grey-darker hover-link"
                href="https://systems.jhu.edu/research/public-health/ncov/"
                target="_blank"
                rel="noopener noreferrer"
              >Johns Hopkins University Center for Systems Science and Engineering (JHU CSSE)</a>
            </p>
  </div>
</template>
<script>
import moment from "moment";

export default {
  name: "CovidStat",
  components: {},
  data() {
    return {
      search: "Kazakhstan",
      myData: [],
      lastUpdate: ""
    };
  },
  created() {
    this.fetchData;
    this.order;
  },
  filters: {
    human_readable(date) {
      return moment.utc(date).format("MM-DD-YYYY, +-HH:mm");
    }
    // iso8601(date) {
    // 	return this.$moment(date).format();
    // }
  },
  computed: {
    filteredList() {
      return this.myData.filter(info => {
        return info.Country.toLowerCase().includes(this.search.toLowerCase());
      });
    },
    async fetchData() {
      fetch("https://api.covid19api.com/summary")
        .then(response => {
          return response.json();
        })
        .then(data => {
          this.myData = data.Countries;
          this.lastUpdate = data.Date;
        });
    }
  }
};
</script>

<style scoped>
@media (min-width: 640px) {
  table {
    display: inline-table !important;
  }

  thead tr:not(:first-child) {
    display: none;
  }
}

td:not(:last-child) {
  border-bottom: 0;
}

th:not(:last-child) {
  border-bottom: 2px solid rgba(0, 0, 0, 0.1);
}
</style>
