<script setup lang="ts">
interface technology {
  id: number
  name: string
  imageUrl: string
}

interface tool {
  id: number
  name: string
  imageUrl: string
}

const tools: tool[] = [
  {
    id: 1,
    name: 'Git',
    imageUrl: 'https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png',
  },
  {
    id: 2,
    name: 'GitHub',
    imageUrl: 'https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png',
  },
  {
    id: 3,
    name: 'Visual Studio Code',
    imageUrl: 'https://code.visualstudio.com/assets/images/code-stable.png',
  },
  {
    id: 4,
    name: 'Node Package Manager',
    imageUrl: 'https://upload.wikimedia.org/wikipedia/commons/thumb/d/db/Npm-logo.svg/810px-Npm-logo.svg.png?20140904162625',
  },
  {
    id: 5,
    name: 'Nmap',
    imageUrl: 'https://nmap.org/images/nmap-logo-64px.svg',
  },
  {
    id: 6,
    name: 'Wireshark',
    imageUrl: '/wireshark.png',
  },
  {
    id: 7,
    name: 'BurpSuite',
    imageUrl: '/burp-suite.svg',
  },
  {
    id: 8,
    name: 'AMASS',
    imageUrl: 'https://avatars.githubusercontent.com/u/128647419?s=48&v=4',
  },
]

const tech: technology[] = [
  {
    id: 1,
    name: 'HTML',
    imageUrl: 'https://cdn-icons-png.flaticon.com/512/1051/1051277.png',
  },
  {
    id: 2,
    name: 'CSS',
    imageUrl: 'https://cdn-icons-png.flaticon.com/512/732/732190.png',
  },
  {
    id: 3,
    name: 'JavaScript',
    imageUrl: 'https://cdn.icon-icons.com/icons2/2415/PNG/512/javascript_original_logo_icon_146455.png',
  },
  {
    id: 4,
    name: 'TypeScript',
    imageUrl: '/ts-logo-256.png',
  },
  {
    id: 5,
    name: 'Vite',
    imageUrl: 'https://upload.wikimedia.org/wikipedia/commons/f/f1/Vitejs-logo.svg',
  },
  {
    id: 6,
    name: 'Vue JS',
    imageUrl: 'https://cdn.iconscout.com/icon/free/png-256/free-vue-282497.png?f=webp',
  },
  {
    id: 7,
    name: 'Node JS',
    imageUrl: 'https://cdn.iconscout.com/icon/free/png-256/free-node-js-1174925.png',
  },
  {
    id: 8,
    name: 'Flutter',
    imageUrl: 'https://storage.googleapis.com/cms-storage-bucket/64d67700f8293a9dc827.svg',
  },
  {
    id: 9,
    name: 'Python',
    imageUrl: 'https://s3.dualstack.us-east-2.amazonaws.com/pythondotorg-assets/media/community/logos/python-logo-only.png',
  },
  {
    id: 10,
    name: 'Tailwind CSS',
    imageUrl: 'https://upload.wikimedia.org/wikipedia/commons/d/d5/Tailwind_CSS_Logo.svg',
  },
  {
    id: 11,
    name: 'Bootstrap',
    imageUrl: 'https://getbootstrap.com/docs/5.2/assets/brand/bootstrap-logo-shadow.png',
  },
  {
    id: 12,
    name: 'Uno CSS',
    imageUrl: 'https://raw.githubusercontent.com/unocss/unocss/main/playground/public/icon-gray.svg',
  },
]
</script>

<template>
  <div
    class="mx-8 mb-5 max-h-auto min-h-[65vh] border border-[#383838] rounded-3xl bg-[#eaddcf] px-5 py-5 text-left md:mt-30 md:max-h-screen md:min-h-[80vh] md:px-12 md:py-10"
  >
    <article data-page="about">
      <header>
        <div class="fadein-bot title-section mb-5 flex items-center text-2xl font-bold text-[#020826]">
          About Me &nbsp;
          <div
            class="aos-init aos-animate h-[1px] w-32 bg-amber-200 md:w-96" data-aos="zoom-in-left"
            data-aos-duration="600"
          />
        </div>
      </header>

      <section
        class="flex flex-col gap-4 text-justify text-sm md:flex-row md:items-center md:justify-center md:gap-8 md:text-lg"
      >
        <div class="flex justify-center">
          <img
            alt="avatar" fetchpriority="high" width="300" height="300" decoding="async" data-nimg="1"
            class="pict h-75 border-4 border-#716040 border-rounded-full md:h-auto" src="/me.jpg"
          >
        </div>
        <div class="md:w-7/12">
          <p class="fadein-left fadeins-1 mb-3 text-[#716040] md:mb-7">
            &nbsp;Hi everyone! My name is AULIA AKBAR.
          </p>
          <p class="fadein-left fadeins-2 mb-3 text-[#716040]">
            &nbsp;I am a seasoned technical support professional with extensive expertise in the electrical (weak current) industries.
            Throughout my career, I have consistently taken the lead in resolving diverse and complex cases.
            Currently, I am pursuing a degree in Computer Science at the university, with a specific focus on Cyber Security.
            I actively engage in activities like CTF (Catch The Flag) challenges and other relevant pursuits, as part of my dedication to becoming a proficient Security Professional.
          </p>
        </div>
      </section>
    </article>
  </div>

  <div class="mx-3 px-5 py-3 text-left text-[#020826] md:px-12 md:py-5">
    <article data-page="about">
      <header>
        <div class="fadein-bot title-section flex items-center text-2xl font-bold text-[#020826]">
          <div
            class="aos-init aos-animate h-[10px] w-10 bg-amber-200 md:w-20" data-aos="zoom-in-left"
            data-aos-duration="600"
          />
          &nbsp; Skills
        </div>
      </header>
      <section>
        <div>
          <ul class="text-md mb-5 flex flex-wrap text-center font-medium text-[#716040]">
            <li class="mr-2">
              <div
                class="inline-block rounded-lg px-4 py-3"
              >
                Tech Stack
              </div>
            </li>
          </ul>
        </div>
        <div>
          <div class="grid grid-cols-2 gap-4 pb-10 md:grid-cols-3 xl:grid-cols-4 2xl:gap-12 md:gap-8 xl:gap-10">
            <div v-for="item in tech" :key="item.id">
              <div
                class="item-tech flex cursor-pointer items-center gap-2 border border-[#8c7851] rounded bg-[#eaddcf] px-2 py-2 md:gap-3 hover:bg-opacity-10 lg:px-3"
              >
                <div class="zoom-in h-12 w-12 flex items-center justify-center p-0 lg:h-16 lg:w-16 lg:p-2">
                  <img
                    alt="HTML" loading="lazy" width="32" height="32" decoding="async" data-nimg="1"
                    class="img-tech h-[65%] w-[65%] drop-shadow-xl transition-all duration-300 lg:h-[85%] lg:w-[85%]"
                    :src="item.imageUrl" style="color: transparent;"
                  >
                </div>
                <div class="flex items-center text-sm lg:text-lg md:text-base">
                  <div class="tech text-secondary translate-y-0 font-medium text-[#020826] transition-all duration-300">
                    {{ item.name }}
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div>
          <ul class="text-size5 text-md mb-5 flex flex-wrap text-center font-medium text-[#716040]">
            <li class="mr-2">
              <div
                class="inline-block rounded-lg px-4 py-3"
              >
                Tools
              </div>
            </li>
          </ul>
        </div>
        <div>
          <div class="grid grid-cols-2 gap-4 pb-10 md:grid-cols-3 xl:grid-cols-4 2xl:gap-12 md:gap-8 xl:gap-10">
            <div v-for="item in tools" :key="item.id">
              <div
                class="item-tech flex cursor-pointer items-center gap-2 border border-[#8c7851] rounded bg-[#eaddcf] px-2 py-2 md:gap-3 hover:bg-opacity-10 lg:px-3"
              >
                <div class="zoom-in h-12 w-12 flex items-center justify-center p-0 lg:h-16 lg:w-16 lg:p-2">
                  <img
                    alt="HTML" loading="lazy" width="32" height="32" decoding="async" data-nimg="1"
                    class="img-tech h-[65%] w-[65%] drop-shadow-xl transition-all duration-300 lg:h-[85%] lg:w-[85%]"
                    :src="item.imageUrl" style="color: transparent;"
                  >
                </div>
                <div class="flex items-center text-sm lg:text-lg md:text-base">
                  <div class="tech text-secondary translate-y-0 font-medium text-[#020826] transition-all duration-300">
                    {{ item.name }}
                  </div>
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
