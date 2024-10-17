<script setup lang='ts'>
import { onMounted, ref, watch } from 'vue'

const toRotate = ['Web Developer', 'Cyber Security Enthusiast', 'Informatics Major']
const period = 2000
const txt = ref('')
const loopNum = ref(0)
const isDeleting = ref(false)

function tick() {
  const i = loopNum.value % toRotate.length
  const fullTxt = toRotate[i]

  if (isDeleting.value)
    txt.value = fullTxt.substring(0, txt.value.length - 1)

  else
    txt.value = fullTxt.substring(0, txt.value.length + 1)

  if (!isDeleting.value && txt.value === fullTxt) {
    isDeleting.value = true
    setTimeout(tick, period)
  }
  else if (isDeleting.value && txt.value === '') {
    isDeleting.value = false
    loopNum.value++
    setTimeout(tick, 500)
  }
  else {
    setTimeout(tick, 200 - Math.random() * 100)
  }
}

onMounted(() => {
  tick()
})

// Watch for changes to the loopNum and reset txt to an empty string
watch(loopNum, () => {
  txt.value = ''
})
</script>

<template>
  <main
    class="max-h-auto min-h-[65vh] flex flex-col-reverse items-center gap-8 md:mt-30 md:max-h-screen md:min-h-[80vh] md:flex-row md:justify-center md:gap-16"
  >
    <div class="px-10 text-center space-y-2 md:text-left">
      <p class="text-size-6 text-#33272a"> ghjgjgjg
        Hello, I'm
      </p>
      <h1 class="fadein-up text-4xl font-bold text-#33272a md:text-5xl">
        AULIA Rahman
      </h1>
      <div class="py-2">
        <h1
          class="typewrite fadein-up from-#33272a to-#33272a bg-gradient-to-r bg-clip-text text-xl font-semibold text-transparent md:text-2xl"
        >
          <span class="wrap">{{ txt }}</span>
        </h1>
      </div>
      <br>
    </div>
    <div class="fadein-right flex justify-center md:justify-start">
      <img
        alt="avatar" fetchpriority="high" width="300" height="300" decoding="async" data-nimg="1"
        class="pict h-75 border-4 border-#716040 border-rounded-full md:h-auto" src="/me.jpg"
      >
    </div>
  </main>
</template>

<style>
body {
  overflow-y: scroll;
  overflow-x: hidden;
}

.typewrite>.wrap {
  border-right: 0.08em solid #fff;
}

.wave {
  animation-name: wave-animation;
  animation-duration: 2.5s;
  animation-iteration-count: infinite;
  transform-origin: 70% 70%;
  display: inline-block
}

@keyframes wave-animation {
  0% {
    transform: rotate(0deg)
  }

  10% {
    transform: rotate(14deg)
  }

  20% {
    transform: rotate(-8deg)
  }

  30% {
    transform: rotate(14deg)
  }

  40% {
    transform: rotate(-4deg)
  }

  50% {
    transform: rotate(10deg)
  }

  60% {
    transform: rotate(0deg)
  }

  to {
    transform: rotate(0deg)
  }
}

.pict {
  box-shadow: 0px 0px 73px -9px rgba(255,219,112,0.44);
-webkit-box-shadow: 0px 0px 73px -9px rgba(255,219,112,0.44);
-moz-box-shadow: 0px 0px 73px -9px rgba(255,219,112,0.44);
}

.fadein-up {
  opacity: 0;
  animation-name: fadeInUp;
  animation-duration: 0.5s;
  animation-fill-mode: forwards;
  animation-delay: 500ms;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translate3d(0, 100%, 0);
  }

  to {
    opacity: 1;
    transform: translate3d(0, 0, 0);
  }
}

.fade-in-from-left {
  opacity: 0;
  animation: fadeInLeft 0.5s ease-out forwards;
  animation-delay: 500ms;
}

@keyframes fadeInLeft {
  0% {
    opacity: 0;
    transform: translateX(-100%);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

.fadein-right {
  opacity: 0;
  animation: fadeInRight 0.5s ease-out forwards;
  animation-delay: 500ms;
}

@keyframes fadeInRight {
  0% {
    opacity: 0;
    transform: translateX(100%);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

.fadein-bot {
  opacity: 0;
  animation: fadeInBot 0.5s forwards;
}

@keyframes fadeInBot {
  from {
    opacity: 0;
    transform: translate3d(0, -100%, 0);
  }

  to {
    opacity: 1;
    transform: translate3d(0, 0, 0);
  }
}

.fadein-1 {
  animation-delay: 200ms;
}
.fadein-2 {
  animation-delay: 400ms;
}
.fadein-3 {
  animation-delay: 600ms;
}
.fade-500 {
  animation-delay: 500ms;
}
</style>
