<template>
  <div class="w-full p-4 text-center">
    <div class="lg:py-12 lg:flex lg:justify-center">
      <img
        src="https://upload.wikimedia.org/wikipedia/commons/e/e7/Kazakhstan_COVID-19_cases_map.svg?uselang=ru"
      />
    </div>

    <div
      class="lg:py-12 lg:flex lg:justify-center"
      data-wikidata-qualifier-id="P2096"
      style="display:block;"
    >
      <p>
        Расшифровка:
        <span style="font-size: 90%; margin: 0px 0px 1px 0px; display: block;">
          <span
            style="vertical-align: top; border: 0px solid #FCEED3; background: #FCEED3; text-align: center;"
            title="#FCEED3"
          >&nbsp;&nbsp;&nbsp;&nbsp;</span>&nbsp;1-2 подтверждённых случаев
        </span>
        <span style="font-size: 90%; margin: 0px 0px 1px 0px; display: block;">
          <span
            style="vertical-align: top; border: 0px solid #F2A88D; background: #F2A88D; text-align: center;"
            title="#F2A88D"
          >&nbsp;&nbsp;&nbsp;&nbsp;</span>&nbsp;3-4 подтверждённых случаев
        </span>
        <span style="font-size: 90%; margin: 0px 0px 1px 0px; display: block;">
          <span
            style="vertical-align: top; border: 0px solid #E36654; background: #E36654; text-align: center;"
            title="#E36654"
          >&nbsp;&nbsp;&nbsp;&nbsp;</span>&nbsp;5-9 подтверждённых случаев
        </span>
        <span style="font-size: 90%; margin: 0px 0px 1px 0px; display: block;">
          <span
            style="vertical-align: top; border: 0px solid #E5354B; background: #E5354B; text-align: center;"
            title="#E5354B"
          >&nbsp;&nbsp;&nbsp;&nbsp;</span>&nbsp;10-24 подтверждённых случаев
        </span>
        <span style="font-size: 90%; margin: 0px 0px 1px 0px; display: block;">
          <span
            style="vertical-align: top; border: 0px solid #87353F; background: #87353F; text-align: center;"
            title="#87353F"
          >&nbsp;&nbsp;&nbsp;&nbsp;</span>&nbsp;25-49 подтверждённых случаев
        </span>
      </p>
      <span style="font-size: 90%; margin: 0px 0px 1px 0px; display: block;">
        <span
          style="vertical-align: top; border: 0px solid #630606; background: #630606; text-align: center;"
          title="#630606"
        >&nbsp;&nbsp;&nbsp;&nbsp;</span>&nbsp;50-99 подтверждённых случаев
      </span>
    </div>
  </div>
</template>

<script>
export default {
  name: "WikiInfo",
  data() {
    return {};
  }
};
</script>
