<template>
  <div class="faq">
    <input id="faq-a" type="checkbox" />
    <label for="faq-a">
      <p
        class="faq-heading"
      >Передача вирусного возбудителя COVID‑19 происходит в районах с жарким влажным климатом.</p>
      <div class="faq-arrow"></div>
      <p class="faq-text">
        По имеющимся в настоящее время данным, передача вирусного возбудителя COVID‑19 может происходить в ЛЮБЫХ РАЙОНАХ, включая районы с жарким влажным климатом.
        <br />
        <br />Если вы проживаете или направляетесь в район, в котором зарегистрированы случаи COVID‑19, принимайте меры защиты вне зависимости от климатических условий.
      </p>
    </label>
    <input id="faq-b" type="checkbox" />
    <label for="faq-b">
      <p
        class="faq-heading"
      >Пребывание на улице в холодную погоду НЕ ПОМОЖЕТ уничтожить коронавирус (2019-nCoV)</p>
      <div class="faq-arrow"></div>
      <p class="faq-text">
        Температура тела здорового человека держится в пределах от 36,5° до 37° независимо от температуры окружающей среды или погоды.
        <br />
        <br />Поэтому нет никаких оснований полагать, что пребывание на улице в холодную погоду помогает бороться с новой коронавирусной инфекцией или другими болезнями.
      </p>
    </label>
    <input id="faq-c" type="checkbox" />
    <label for="faq-c">
      <p class="faq-heading">Горячая ванна НЕ ПОМОЖЕТ против новой коронавирусной инфекции</p>
      <div class="faq-arrow"></div>
      <p class="faq-text">
        Прием горячей ванны не спасет от заражения COVID-19. Нормальная температура тела держится в пределах от 36,5°C до 37°C независимо от температуры воды в ванне или душе.
        <br />
        <br />Напротив, принятие слишком горячей ванны может нанести вред и вызвать ожоги.
      </p>
    </label>
    <input id="faq-d" type="checkbox" />
    <label for="faq-d">
      <p class="faq-heading">Коронавирус НЕ ПЕРЕДАЕТСЯ через укусы комаров</p>
      <div class="faq-arrow"></div>
      <p class="faq-text">
        Коронавирус – респираторный вирус, главным образом передающийся воздушно-капельным путем, т.е. в результате вдыхания капель, выделяемых из дыхательных путей больного, например при кашле или чихании, а также капель слюны или выделений из носа.
        <br />
        <br />На данный момент информация о возможности передачи вируса 2019-nCoV через укусы комаров отсутствует.
      </p>
    </label>
    <input id="faq-e" type="checkbox" />
    <label for="faq-e">
      <p
        class="faq-heading"
      >Насколько эффективно теловые сканеры позволяют выявлять зараженных коронавирусом?</p>
      <div class="faq-arrow"></div>
      <p class="faq-text">
        Тепловые сканеры позволяют эффективно обнаруживать тех людей, у которых в результате заражения новым коронавирусом (COVID-19) развилась лихорадка (повышена температура тела).
        <br />
        <br />Однако выявить зараженных людей до стадии лихорадки с помощью этой технологии нельзя. С момента заражения до повышения температуры проходит от двух до десяти дней.
      </p>
    </label>
    <input id="settings" type="checkbox" />
    <input id="faq-f" type="checkbox" />
    <label for="faq-f">
      <p
        class="faq-heading"
      >Обработка поверхности всего тела этанолом или хлорной известью позволяет уничтожить новый коронавирус</p>
      <div class="faq-arrow"></div>
      <p class="faq-text">
        Нет. Обработка всего тела спиртом или хлорной известью не уничтожит вирусы, которые уже проникли в организм. Распыление таких веществ может нанести вред одежде и слизистым оболочкам (т.е. глазам, ротовой полости).
        <br />
        <br />Следует помнить, что как спирт, так и хлорная известь, могут быть эффективными средствами дезинфекции поверхностей, но использовать их необходимо в соответствующих случаях и с соблюдением правил.
        <br />
      </p>
    </label>
  </div>
</template>

<script>
export default {
  name: "Myth",
  data() {
    return {};
  }
};
</script>

<style scoped>
.faq-heading {
  font-weight: 400;
  font-size: 19px;
  -webkit-transition: text-indent 0.2s;
  /* text-indent: 20px; */
  color: #333;
  width: 95%;
  padding-left: 20px;
  margin-bottom: 30px;
}

.faq-text {
  font-family: Open Sans;
  font-weight: 400;
  color: #919191;
  width: 95%;
  padding-left: 20px;
  margin-bottom: 2rem !important;
}

.faq {
  width: 100%;
  margin: 0 auto;
  background: white;
  border-radius: 4px;
  position: relative;
  border: 1px solid #e1e1e1;
}
.faq label {
  display: block;
  position: relative;
  overflow: hidden;
  cursor: pointer;
  height: 56px;
  padding-top: 1px;
  background-color: #fafafa;
  border-bottom: 1px solid #e1e1e1;
}

.faq input[type="checkbox"] {
  display: none;
}

.faq .faq-arrow {
  width: 8px;
  height: 8px;
  transition: -webkit-transform 0.8s;
  transition: transform 0.8s;
  transition: transform 0.8s, -webkit-transform 0.8s;
  -webkit-transition-timing-function: cubic-bezier(0.68, -0.55, 0.265, 1.55);
  border-top: 2px solid rgba(0, 0, 0, 0.33);
  border-right: 2px solid rgba(0, 0, 0, 0.33);
  float: right;
  position: relative;
  top: -2.9rem;
  right: 1rem;
  -webkit-transform: rotate(45deg);
  transform: rotate(45deg);
}

.faq input[type="checkbox"]:checked + label > .faq-arrow {
  transition: -webkit-transform 0.8s;
  transition: transform 0.8s;
  transition: transform 0.8s, -webkit-transform 0.8s;
  -webkit-transition-timing-function: cubic-bezier(0.68, -0.55, 0.265, 1.55);
  -webkit-transform: rotate(135deg);
  transform: rotate(135deg);
}
.faq input[type="checkbox"]:checked + label {
  display: block;
  background: rgba(255, 255, 255, 255) !important;
  color: #4f7351;
  height: 280px;
  transition: height 0.8s;
  -webkit-transition-timing-function: cubic-bezier(0.68, -0.55, 0.265, 1.55);
}

.faq input[type="checkbox"]:not(:checked) + label {
  display: block;
  transition: height 0.8s;
  height: 60px;
  -webkit-transition-timing-function: cubic-bezier(0.68, -0.55, 0.265, 1.55);
}

::-webkit-scrollbar {
  display: none;
}
</style>