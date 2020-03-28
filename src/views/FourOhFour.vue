<template>
<body class="antialiased font-sans">
  <div class="md:flex">
    <div class="w-full md:w-1/2 md:h-screen bg-white flex items-center justify-center">
      <div class="max-w-sm m-8">
        <div class="text-black text-5xl md:text-15xl font-black">404</div>
        <div class="w-16 h-1 bg-blue-dark my-3 md:my-6"></div>
        <p
          class="text-grey-darker text-2xl md:text-3xl font-light mb-8 leading-normal"
        >Извините, страница которую вы ищите не найдена.</p>
        <router-link to="/">
          <button
            class="bg-transparent text-grey-darkest font-bold uppercase tracking-wide py-3 px-6 border-2 border-grey-light hover:border-grey rounded-lg"
          >Вернутся на главную</button>
        </router-link>
      </div>
    </div>
    <div  
      style="background-image: url('src/assets/svg/undraw_page_not_found_su7k.svg');"
      class="max-w-full md:w-1/2 h-screen md:bg-cover bg-no-repeat md:bg-left lg:bg-center"
    ></div>
  </div>
</body>
</template>