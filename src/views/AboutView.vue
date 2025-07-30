<script>
export default {
  data() {
    return {
      activeTab: 1,
      tech: [
        {
          id: 1,
          name: 'HTML',
          imageUrl: 'https://cdn-icons-png.flaticon.com/512/1051/1051277.png',
          status: 'intermediario'
        },
        {
          id: 2,
          name: 'CSS',
          imageUrl: 'https://cdn-icons-png.flaticon.com/512/732/732190.png',
          status: 'intermediario'
        },
        //{
        //  id: 3,
        //  name: 'PHP',
        //  imageUrl: 'https://cdn.iconscout.com/icon/free/png-256/free-php-2038871-1720084.png',
        // status: 'Advanced'
        //},
        {
          id: 4,
          name: 'Javascript',
          imageUrl: 'https://cdn.icon-icons.com/icons2/2415/PNG/512/javascript_original_logo_icon_146455.png',
          status: 'iniciante'
        },
        {
          id: 5,
          name: 'Phython',
          imageUrl: 'https://s3.dualstack.us-east-2.amazonaws.com/pythondotorg-assets/media/community/logos/python-logo-only.png',
          status: 'intermediario'
        },
        //{
        //  id: 5,
        //  name: 'Laravel',
        //  imageUrl: 'https://cdn.worldvectorlogo.com/logos/laravel-2.svg',
        //  status: 'Advance'
        //},
        //{
        //  id: 6,
        //  name: 'Codeigniter',
        //  imageUrl: 'https://cdn-peanutsquare.b-cdn.net/wp-content/uploads/2022/11/codeigniter-logo.png',
        //  status: 'Intermediate'
        //},
        //{
        //  id: 7,
        //  name: 'VueJS',
        //  imageUrl: 'https://cdn.iconscout.com/icon/free/png-256/free-vue-282497.png?f=webp',
        //  status: 'Intermediate'
        //},
        //{
        // id: 8,
        //  name: 'AlpineJS',
        // imageUrl: 'https://avatars.githubusercontent.com/u/59030169?s=200&v=4',
        //  status: 'Beginner'
        //},
        //{
        //  id: 9,
        //  name: 'NodeJS',
        //  imageUrl: 'https://cdn.iconscout.com/icon/free/png-256/free-node-js-1174925.png',
        //  status: 'Beginner'
        //},
        //{
        //  id: 10,
        //  name: 'Tailwind',
        //  imageUrl: 'https://upload.wikimedia.org/wikipedia/commons/d/d5/Tailwind_CSS_Logo.svg',
        //  status: 'Advance'
        //},
        {
          id: 1,
          name: 'Bootstrap',
          imageUrl: 'https://getbootstrap.com/docs/5.2/assets/brand/bootstrap-logo-shadow.png',
          status: ''
        },
        //{
        //  id: 12,
        //  name: 'ReactJS',
        //  imageUrl: 'https://cdn4.iconfinder.com/data/icons/logos-3/600/React.js_logo-512.png',
        //  status: 'Beginner'
        //}
      ],
      tools: [
        {
          id: 1,
          name: 'Git',
          imageUrl: 'https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png',
          status: ''
        },
        {
          id: 2,
          name: 'GitHub',
          imageUrl: 'https://cdn-icons-png.flaticon.com/512/25/25231.png',
          status: ''
        },
        //{
        //  id: 3,
        //  name: 'NPM',
        //  imageUrl: 'https://cdn.iconscout.com/icon/free/png-256/free-npm-3-1175132.png',
        //  status: 'Package Manager'
        //},
        {
          id: 4,
          name: 'MySQL',
          imageUrl: 'https://cdn-icons-png.flaticon.com/512/5968/5968313.png',
          status: ''
        },
        {
          id: 5,
          name: 'Docker Desktop',
          imageUrl: 'data:image/png;base64,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',
          status: ''
        },
        {
          id: 6,
          name: 'POSTEGREE',
          imageUrl: 'https://www.postgresql.org/media/img/about/press/elephant.png',
          status: ''
        },
      ]
    };
  }
}
</script>
<template>
  <div
    class="bg-[#1e1e1f] px-5 py-5 md:px-12 md:py-10 text-left border border-[#383838] rounded-3xl text-amber-50 mx-3 mb-5">
    <article data-page="about">

      <header>
        <div class="text-2xl font-bold text-white mb-5 fadein-bot title-section flex items-center">
          Sobre Mim &nbsp;
          <div class="h-[1px] w-32 bg-amber-200 md:w-96 aos-init aos-animate" data-aos="zoom-in-left"
            data-aos-duration="600"></div>
        </div>
      </header>

      <section
        class="text-sm md:text-lg text-justify flex flex-col gap-4 md:flex-row md:gap-8 md:justify-left md:items-center">
        <div class="flex justify-center">
          <img class="md:h-auto rounded-full border-4 border-amber-200 pict"
            src="/img/eu.jpg" alt="Foto">
        </div>
        <div class="md:w-7/12">
          <p class="mb-3 md:mb-7 fadein-left fadeins-1">
            &nbsp; &nbsp; &nbsp; Sou um estudante dedicado de Engenharia de Software, apaixonado por tecnologia e determinado a aprender e crescer na área. Embora esteja no início do meu curso, estou entusiasmado em desenvolver habilidades sólidas em programação e análise de sistemas.
            Estou atualmente estagiando na CGM (Controladoria geral de saquarema ) da prefeitura de saquarema, Criando alguns sistemas e automatizaçoes. 
          </p>
          <p class="mb-3 fadein-left fadeins-2">
            &nbsp; &nbsp; &nbsp; Sou uma pessoa comprometida, disposta a enfrentar desafios e aprender com eles.Estou aberto a aprender novas linguagens de programação, ferramentas e metodologias,
             e estou ansioso para trabalhar em equipe e contribuir para projetos significativos na área de engenharia de software. Estou determinado a me tornar um profissional qualificado e contribuir para o avanço da tecnologia.
          </p>
        </div>

      </section>

    </article>
  </div>

  <div class="px-5 py-5 md:px-12 md:py-10 text-left text-amber-50 mx-3">
    <article data-page="about">
      <header>
        <div class="text-2xl font-bold text-white mb-5 fadein-bot title-section flex items-center">
          <div class="h-[1px] w-10 bg-amber-200 md:w-20 aos-init aos-animate" data-aos="zoom-in-left"
            data-aos-duration="600"></div>
          &nbsp; Skills
        </div>
      </header>
      <section>
        <div>
          <ul class="flex flex-wrap text-sm font-medium text-center text-gray-500 dark:text-gray-400 mb-5">
            <li class="mr-2">
              <button class="inline-block px-4 py-3 rounded-lg hover:text-white"
                :class="{ 'text-amber-200 bg-amber-200 bg-opacity-10': activeTab === 1 }" @click="activeTab = 1">Tech Stack</button>
            </li>
            <li class="mr-2">
              <button class="inline-block px-4 py-3 rounded-lg hover:text-white"
                :class="{ 'text-amber-200 bg-amber-200 bg-opacity-10': activeTab === 2 }" @click="activeTab = 2">Tools</button>
            </li>
          </ul>
        </div>
        <div v-show="activeTab === 1">
          <div class="grid grid-cols-2 gap-4 pb-32 md:grid-cols-3 md:gap-8 xl:grid-cols-4 xl:gap-10 2xl:gap-12">
            <div v-for="item in tech" :key="item.id">
              <div
                class="item-tech flex cursor-pointer items-center gap-2 rounded border border-amber-200 px-2 py-2 hover:bg-amber-200 hover:bg-opacity-10 md:gap-3 lg:px-3">
                <div class="flex h-12 w-12 items-center justify-center p-0 lg:h-16 lg:w-16 lg:p-2 zoom-in">
                  <img alt="HTML" loading="lazy" width="32" height="32" decoding="async" data-nimg="1"
                    class="img-tech drop-shadow-xl transition-all duration-300 h-[65%] w-[65%] lg:h-[85%] lg:w-[85%]  "
                    :src="item.imageUrl" style="color: transparent;">
                </div>
                <div class="flex items-center text-sm md:text-base lg:text-lg">
                  <div class="tech font-medium text-secondary transition-all duration-300 translate-y-0 ">{{ item.name }}
                  </div>
                  <div
                    class="status-tech opacity-0 absolute mt-5 text-[10px] text-amber-200 transition-all duration-300 md:text-xs lg:text-sm">
                    {{ item.status }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div v-show="activeTab === 2">
          <div class="grid grid-cols-2 gap-4 pb-32 md:grid-cols-3 md:gap-8 xl:grid-cols-4 xl:gap-10 2xl:gap-12">
            <div v-for="item in tools" :key="item.id">
              <div
                class="item-tech flex cursor-pointer items-center gap-2 rounded border border-amber-200 px-2 py-2 hover:bg-amber-200 hover:bg-opacity-10 md:gap-3 lg:px-3">
                <div class="flex h-12 w-12 items-center justify-center p-0 lg:h-16 lg:w-16 lg:p-2 zoom-in">
                  <img alt="HTML" loading="lazy" width="32" height="32" decoding="async" data-nimg="1"
                    class="img-tech drop-shadow-xl transition-all duration-300 h-[65%] w-[65%] lg:h-[85%] lg:w-[85%]  "
                    :src="item.imageUrl" style="color: transparent;">
                </div>
                <div class="flex items-center text-sm md:text-base lg:text-lg">
                  <div class="tech font-medium text-secondary transition-all duration-300 translate-y-0 ">{{ item.name }}
                  </div>
                  <div
                    class="status-tech opacity-0 absolute mt-5 text-[10px] text-amber-200 transition-all duration-300 md:text-xs lg:text-sm">
                    {{ item.status }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </article>
  </div>
</template>

<style>
.fadein-left {
  opacity: 0;
  animation: fadeInLeft 0.5s ease-out forwards;
}

@keyframes fadeInLeft {
  0% {
    opacity: 0;
    transform: translateX(100%);
  }

  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

.fadeins-1 {
  animation-delay: 500ms;
}

.fadeins-2 {
  animation-delay: 800ms;
}

.img-tech,
.tech {
  transition: transform 0.3s ease;
}

.item-tech:hover .img-tech {
  transform: scale(1.3);
}

.item-tech:hover .tech {
  transform: translateY(-12px);
}

.item-tech:hover .status-tech {
  opacity: 1;
}
</style>
