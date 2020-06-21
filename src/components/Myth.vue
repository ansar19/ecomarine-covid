<template>
  <div class="row">
    <div class="grid col-gap-2 grid-cols-1">
      <div class="tabs">
        <div class="tab">
          <input type="checkbox" id="chck1" />
          <label
            class="tab-label"
            for="chck1"
          >Передача вирусного возбудителя COVID‑19 происходит в районах с жарким влажным климатом.</label>
          <div class="tab-content">
            <p class="faq-text">
              По имеющимся в настоящее время данным, передача вирусного возбудителя COVID‑19 может происходить в ЛЮБЫХ РАЙОНАХ, включая районы с жарким влажным климатом.
              <br />
              <br />Если вы проживаете или направляетесь в район, в котором зарегистрированы случаи COVID‑19, принимайте меры защиты вне зависимости от климатических условий.
            </p>
          </div>
        </div>
        <div class="tab">
          <input type="checkbox" id="chck2" />
          <label
            class="tab-label"
            for="chck2"
          >Пребывание на улице в холодную погоду помогает уничтожить коронавирус</label>
          <div class="tab-content">
            <p class="faq-text">
              Температура тела здорового человека держится в пределах от 36,5° до 37° независимо от температуры окружающей среды или погоды.  
              <br />
              <br />Поэтому нет никаких оснований полагать, что пребывание на улице в холодную погоду помогает бороться с новой коронавирусной инфекцией или другими болезнями. Самым эффективным способом профилактики новой коронавирусной инфекции (2019-nCoV) является регулярная обработка рук спиртосодержащим антисептиком или их мытье водой с мылом.
            </p>
          </div>
        </div>

        <div class="tab">
          <input type="checkbox" id="chck3" />
          <label
            class="tab-label"
            for="chck3"
          >Горячая ванна помогает против новой коронавирусной инфекции</label>
          <div class="tab-content">
            <p class="faq-text">
              Прием горячей ванны НЕ СПАСАЕТ от заражения COVID-19. Нормальная температура тела держится в пределах от 36,5°C до 37°C независимо от температуры воды в ванне или душе.
              <br />
              <br />Напротив, принятие слишком горячей ванны может нанести вред и вызвать ожоги.
            </p>
          </div>
        </div>

        <div class="tab">
          <input type="checkbox" id="chck4" />
          <label class="tab-label" for="chck4">Коронавирус передается через укусы комаров</label>
          <div class="tab-content">
            <p class="faq-text">
              Коронавирус – респираторный вирус, главным образом передающийся воздушно-капельным путем, т.е. в результате вдыхания капель, выделяемых из дыхательных путей больного, например при кашле или чихании, а также капель слюны или выделений из носа.
              <br />
              <br />На данный момент информация о возможности передачи вируса COVID‑19 через укусы комаров отсутствует.
            </p>
          </div>
        </div>

        <div class="tab">
          <input type="checkbox" id="chck5" />
          <label
            class="tab-label"
            for="chck5"
          >Обработка поверхности всего тела этанолом или хлорной известью позволяет уничтожить новый коронавирус</label>
          <div class="tab-content">
            <p class="faq-text">
              Нет. Обработка всего тела спиртом или хлорной известью не уничтожит вирусы, которые уже проникли в организм. Распыление таких веществ может нанести вред одежде и слизистым оболочкам (т.е. глазам, ротовой полости).
              <br />
              <br />Следует помнить, что как спирт, так и хлорная известь, могут быть эффективными средствами дезинфекции поверхностей, но использовать их необходимо в соответствующих случаях и с соблюдением правил.
              <br />
            </p>
          </div>
        </div>

        <div class="tab">
          <input type="checkbox" id="chck6" />
          <label
            class="tab-label"
            for="chck6"
          >Насколько эффективно тепловые сканеры позволяют выявлять зараженных коронавирусом?</label>
          <div class="tab-content">
            <p class="faq-text">
              Тепловые сканеры позволяют эффективно обнаруживать тех людей, у которых в результате заражения новым коронавирусом (COVID-19) развилась лихорадка (повышена температура тела).
              <br />
              <br />Однако выявить зараженных людей до стадии лихорадки с помощью этой технологии нельзя. С момента заражения до повышения температуры проходит от двух до десяти дней.
            </p>
          </div>
        </div>

        <div class="tab">
          <input type="checkbox" id="chck7" />
          <label
            class="tab-label"
            for="chck7"
          >Добавление перца в суп или другие блюда НЕ защищает и НЕ излечивает от COVID‑19</label>
          <div class="tab-content">
            <p class="faq-text">
              Пикантный перец в пище, безусловно, обладает гастрономическими достоинствами, но не предотвращает и не излечивает от COVID‑19. 
              <br />
              <br />Лучший способ защиты от новой коронавирусной инфекции – соблюдение дистанции не менее одного метра от окружающих, а также частое и тщательное мытье рук. Кроме того, благоприятным общеукрепляющим действием обладают сбалансированное питание, достаточное потребление жидкости, регулярные физические упражнения и здоровый сон.
            </p>
          </div>
        </div>

        <div class="tab">
          <input type="checkbox" id="chck8" />
          <label
            class="tab-label"
            for="chck8"
          >Ультрафиолетовые (УФ) лампы не следует использовать для дезинфекции рук или кожи на других участках тела</label>
          <div class="tab-content">
            <p class="faq-text">
              Уф‑излучение способно приводить к раздражению кожи и вызывать повреждение глаз.  
              <br />
              <br />Самыми эффективными способами удаления вирусных частиц являются использование спиртосодержащих средств для обработки рук и мытье рук с мылом. 
            </p>
          </div>
        </div>

        
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Myth",
  data() {
    return {};
  },
  methods: {}
};
</script>

<style scoped>
body {
  padding: 0 1em 1em;
}
h1 {
  margin: 0;
  line-height: 2;
  text-align: center;
}
h2 {
  margin: 0 0 0.5em;
  font-weight: normal;
}
input {
  position: absolute;
  opacity: 0;
  z-index: -1;
}

.row {
  display: flex;
}
.row .col {
  flex: 1;
}
.row .col:last-child {
  margin-left: 1em;
}
/* Accordion styles */
.tabs {
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 4px 4px -2px rgba(0, 0, 0, 0.5);
}
.tab {
  width: 100%;
  color: white;
  overflow: hidden;
}
.tab-label {
  display: flex;
  justify-content: space-between;
  padding: 1em;
  background: #444;
  font-weight: bold;
  cursor: pointer;
  /* Icon */
}
.tab-label:hover {
  background: #0fbf96;
}
.tab-label::after {
  content: "\276F";
  width: 1em;
  height: 1em;
  text-align: center;
  transition: all 0.35s;
}
.tab-content {
  max-height: 0;
  padding: 0 1em;
  color: #444;
  background: white;
  transition: all 0.35s;
}
.tab-close {
  display: flex;
  justify-content: flex-end;
  padding: 1em;
  font-size: 0.75em;
  background: #444;
  cursor: pointer;
}
.tab-close:hover {
  background: #0fbf96;
}
input:checked + .tab-label {
  background: #0fbf96;
}
input:checked + .tab-label::after {
  transform: rotate(90deg);
}
input:checked ~ .tab-content {
  max-height: 100vh;
  padding: 1em;
}
</style>