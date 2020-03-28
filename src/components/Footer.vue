<template>
  <div class="pt-24 pb-20 md:pb-16 bg-white p-8 background--alt">
    <div class="container mx-auto text-left opacity-100 text-sm lg:px-4">
      <div class="flex flex-col justify-center items-start content-start lg:flex-row mb-4">
        <div class="mb-6 md:mb-0 sm:w-1/4 h-auto">
          <a
            v-scroll-reveal="{ delay: 1000, distance: '5%' }"
            class="cursor-pointer inline-block w-20"
            href="/"
            rel="noopener noreferrer"
          >
            <img
              alt="EcoMarine Icon"
              class="w-full grow"
              src="@/assets/img/ecomarine-rus-1357x889.png"
            />
          </a>
          <p
            class="mt-32 text-left text-grey text-sm opacity-50 hidden lg:block"
          >© EcoMarine.kz Kazakhstan {{ currentYear }}</p>
        </div>
        <div class="sm:w-1/4 h-auto sm:mt-0 mt-8">
          <div class="text-lg text-grey-darkest mb-4">Ссылки</div>
          <ul class="list-reset leading-normal cursor-pointer">
            <li class="mb-4 md:mb-2">
              <a
                class="link open-sans-regular text-grey-darker hover-link"
                href="https://ecomarine.kz/"
                target="_blank"
                rel="noopener noreferrer"
              >Сайт ecomarine.kz</a>
            </li>
            <li class="mb-4 md:mb-2">
              <a
                class="link open-sans-regular text-grey-darker hover-link"
                href="https://ecomarine.kz/blog"
                target="_blank"
                rel="noopener noreferrer"
              >Блог EcoMarine</a>
            </li>
            <li class="mb-4 md:mb-2">
              <a
                class="link open-sans-regular text-grey-darker hover-link"
                href="mailto:info@ecomarine.kz"
                target="_blank"
                rel="noopener noreferrer"
              >Написать нам</a>
            </li>
            <li class="mb-4 md:mb-2">
              <a
                class="link open-sans-regular text-grey-darker hover-link"
                href="https://ru.wikipedia.org/wiki/%D0%A0%D0%B0%D1%81%D0%BF%D1%80%D0%BE%D1%81%D1%82%D1%80%D0%B0%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5_COVID-19_%D0%B2_%D0%9A%D0%B0%D0%B7%D0%B0%D1%85%D1%81%D1%82%D0%B0%D0%BD%D0%B5"
                target="_blank"
                rel="noopener noreferrer"
              >COVID-19 Казахстан на Википедии</a>
            </li>
            <li class="mb-4 md:mb-2">
              <a
                class="link open-sans-regular text-grey-darker hover-link"
                href="https://www.who.int/ru/emergencies/diseases/novel-coronavirus-2019/advice-for-public"
                target="_blank"
                rel="noopener noreferrer"
              >ВОЗ</a>
            </li>
            <li class="mb-4 md:mb-2">
              <a
                class="link open-sans-regular text-grey-darker hover-link"
                href="https://www.flaticon.com/authors/freepik"
                target="_blank"
                rel="noopener noreferrer"
              >Иконки созданы&nbsp;Freepik</a>
            </li>
          </ul>
        </div>
        <div class="sm:w-1/4 h-auto mt-8 lg:mt-0">
          <div class="text-lg text-grey-darkest mb-4">Медиа</div>
          <ul class="list-reset leading-normal cursor-pointer">
            <li class="mb-4 md:mb-2">
              <a
                class="link open-sans-regular text-grey-darker hover-link"
                href="https://t.me/ecomarinekz"
                target="_blank"
                rel="noopener noreferrer"
              >Telegram</a>
            </li>
            <li class="mb-4 md:mb-2">
              <a
                class="link open-sans-regular text-grey-darker hover-link"
                href="https://twitter.com/ecomarinekz"
                target="_blank"
                rel="noopener noreferrer"
              >Twitter</a>
            </li>
            <li class="mb-4 md:mb-2">
              <a
                class="link open-sans-regular text-grey-darker hover-link"
                href="https://www.instagram.com/ecomarinekz"
                target="_blank"
                rel="noopener noreferrer"
              >Instagram</a>
            </li>
            <li class="mb-4 md:mb-2">
              <a
                class="link open-sans-regular text-grey-darker hover-link"
                href="https://www.facebook.com/ecomarinekz"
                target="_blank"
                rel="noopener noreferrer"
              >Facebook</a>
            </li>
            <li class="mb-4 md:mb-2">
              <a
                class="link open-sans-regular text-grey-darker hover-link"
                href="https://medium.com/@ecomarinekz"
                target="_blank"
                rel="noopener noreferrer"
              >Medium</a>
            </li>
          </ul>
        </div>
        <div>
          <transition appear name="fade">
            <div class="mt-12 mt-4 lg:mt-0">
              <div class="text-lg text-grey-darkest mb-4">Написать</div>
              <a
                class="link open-sans-regular text-grey-darker hover-link opacity-100 inline-block w-8 mr-6 md:mr-4 grow"
                href="mailto:info@ecomarine.kz"
                target="_blank"
                rel="noopener noreferrer"
              >info@ecomarine.kz</a>
            </div>
          </transition>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      currentYear: new Date().getFullYear()
    };
  }
};
</script>
