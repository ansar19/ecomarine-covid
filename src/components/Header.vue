<template>
  <div class="background--alt">
    <nav
      class="container mx-auto flex items-center justify-between flex-wrap pt-8 px-6 md:px-12"
    >
      <div class="flex items-center flex-shrink-0 text-black mr-6">
        <transition appear name="fadeDown">
          <a
            class="cursor-pointer inline-block w-20 grow"
            href="/"
            rel="noopener noreferrer"
          >
            <img
              alt="EcoMarine Icon"
              class="w-20"
              src="@/assets/img/ecomarine-rus-1357x889.png"
            />
          </a>
        </transition>
      </div>
      <div class="hidden lg:block lg:inline-flex lg:items-center lg:w-auto">
        <div class="text-sm lg:flex-grow">
          <a
            href="#covid-calc"
            v-smooth-scroll="{ duration: 1000 }"
            class="block mt-4 lg:inline-block lg:mt-0 cursor-pointer text-black hover-link mr-5"
          >
            Калькулятор
          </a>
          <a
            href="#map"
            v-smooth-scroll="{ duration: 1000 }"
            class="block mt-4 lg:inline-block lg:mt-0 cursor-pointer text-black hover-link mr-5"
          >
            Карта
          </a>
          <a
            href="#precaution"
            v-smooth-scroll="{ duration: 1000, offset: 50 }"
            class="block mt-4 lg:inline-block lg:mt-0 cursor-pointer text-black hover-link mr-5"
          >
            Меры предосторожности
          </a>
          
          <a
            href="#myth"
            v-smooth-scroll="{ duration: 1000 }"
            class="block mt-4 lg:inline-block lg:mt-0 cursor-pointer text-black hover-link mr-5"
          >
            Мифы и ложные представления
          </a>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: "Header"
};
</script>
