<template>
  <div class>
    <div class="info-box">
      <div class="page-wrapper">
        <div class="box shadow-lg">
          <div class="box__content">
            <img src="https://image.flaticon.com/icons/svg/2746/2746339.svg" alt="hand wash" />
            <p>Мойте руки с водой и мылом не менее 20 секунд или обрабатывайте руки спиртосодержащим антисептиком.</p>
          </div>
        </div>
        <div class="box shadow-lg">
          <div class="box__content">
            <img
              src="https://image.flaticon.com/icons/svg/2599/2599547.svg"
              alt="sneezing and coughing"
            />
            <p>Прикрывайте рот и нос платком или согнутым локтем при кашле или чихании.</p>
          </div>
        </div>
        <div class="box shadow-lg">
          <div class="box__content">
            <img src="https://image.flaticon.com/icons/svg/655/655820.svg" alt="avoid travelling" />
            <p>Избегайте поездок, особенно если у вас жар или простуда.</p>
          </div>
        </div>
        <div class="box shadow-lg">
          <div class="box__content">
            <img src="https://image.flaticon.com/icons/svg/709/709072.svg" alt="seek health" />
            <p>Если у вас жар, кашель и затрудненное дыхание, обратитесь за медицинской помощью.</p>
          </div>
        </div>
        <div class="box shadow-lg">
          <div class="box__content">
            <img src="https://image.flaticon.com/icons/svg/2599/2599564.svg" alt="medical mask" />
            <p>Если вы кашляете и чихаете, носите маску и обязательно узнайте, как ее использовать, дезинфицировать и утилизировать.</p>
          </div>
        </div>
        <div class="box shadow-lg">
          <div class="box__content">
            <img src="https://image.flaticon.com/icons/svg/2746/2746334.svg" alt="keep distance" />
            <p>Держитесь от людей на расстоянии как минимум 1 метра, особенно если у них кашель, насморк и повышенная температура.</p>
          </div>
        </div>
        <div class="box shadow-lg">
          <div class="box__content">
            <img src="https://image.flaticon.com/icons/svg/2746/2746337.svg" alt="stay at home" />
            <p>Оставайтесь дома и избегайте контактов.</p>
          </div>
        </div>
        <div class="box shadow-lg">
          <div class="box__content">
            <img
              src="https://image.flaticon.com/icons/svg/2746/2746442.svg"
              alt="don't touch your face"
            />
            <p>Наши руки касаются многих поверхностей, на которых может присутствовать вирус и трогая лицо, мы можем занести его через слизистые глаз, реже трогайте лицо и глаза.</p>
          </div>
        </div>
        <div class="box shadow-lg">
          <div class="box__content">
            <img
              src="https://image.flaticon.com/icons/svg/2729/2729036.svg"
              alt="education, training and hobby"
            />
            <p>Займитесь самообразованием, тренировками или любимым хобби.</p>
          </div>
        </div>
        <div class="box shadow-lg">
          <div class="box__content">
            <img
              src="https://image.flaticon.com/icons/svg/2729/2729078.svg"
              alt="keep windows clean"
            />
            <p>Чаще проводите влажную уборку в помещении, мойте окна, помните солнечные лучи убивают микроорганизмы.</p>
          </div>
        </div>
        <div class="box shadow-lg">
          <div class="box__content">
            <img src="https://image.flaticon.com/icons/svg/2746/2746327.svg" alt="no hand shake" />
            <p>Воздержитесь от рукопожатий, в знак приветствия машите рукой, делайте кивок или поклон.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
:root {
  --dark: #444;
  --darker: #333;
  --light: #eee;
}

*,
*::berofe,
*::after {
  box-sizing: border-box;
  /* marign: 0;
  padding: 0; */
}

/* html {
  font-size: 62.5%;
} */

.info-box {
  display: grid;
  justify-content: center;
  align-items: center;
  font-size: 1rem;
  min-height: 100vh;
}

.page-wrapper {
  max-width: 100%;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  grid-auto-flow: dense;
  grid-gap: 2rem;
  margin-left: 2rem;
  margin-right: 2rem;
  padding-left: 2rem;
  padding-right: 2rem;
}

.box {
  display: grid;
  place-content: center;
  background-color: var(--dark);
  color: var(--light);
  padding: 1rem;
}

.box:nth-child(1),
.box:nth-child(6) {
  grid-column: span 2;
  grid-row: span 1;
}

.box:nth-child(2) {
  grid-column: span 1;
  grid-row: span 2;
}

.box:nth-child(3),
.box:nth-child(4),
.box:nth-child(5),
.box:nth-child(7) {
  grid-column: span 1;
  grid-row: span 1;
}

.box__content {
  text-align: center;
}

.box__content img {
  max-width: 90px;
  max-height: 90px;
  margin-bottom: 1rem;
  display: inline-block;
}

@media (max-width: 1112px) {
  .box:nth-child(6) {
    grid-column: span 3;
  }

  .box:nth-child(7) {
    grid-row: span 2;
  }
}

@media (max-width: 892px) {
  .box:nth-child(2) {
    grid-row: span 2;
  }

  .box:nth-child(4) {
    grid-row: span 2;
  }

  .box:nth-child(6) {
    grid-column: span 2;
  }
}

@media (max-width: 682px) {
  .page-wrapper {
    display: flex;
    flex-direction: column;
  }
}
</style>
