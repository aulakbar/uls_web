<script setup lang="ts">
</script>

<template>
  <div class="relative mx-auto mb-10 flex flex-col md:relative md:mx-auto md:mb-10">
    <nav
      class="top-0 z-[98] w-screen bg-[#121212] bg-opacity-80 px-5 backdrop-blur-md md:fixed"
    >
      <div class="flex flex-wrap items-center justify-center">
        <div
          id="mobile-menu-3"
          class="w-auto flex items-center justify-between md:order-1 md:w-auto md:flex"
        >
          <ul
            class="mt-4 flex flex-row md:mt-0 md:flex-row space-x-8 md:text-lg md:font-medium md:space-x-20"
          >
            <li>
              <router-link
                to="/"
                class="fadein-bot block py-2 pl-3 pr-4 text-#fffffe md:border-0 hover:bg-gray-50 md:p-0 md:hover:bg-transparent md:hover:text-#8c7851"
                aria-current="page"
              >
                Home
              </router-link>
            </li>
            <li>
              <router-link
                to="/about"
                class="fadein-bot block py-2 pl-3 pr-4 text-#fffffe md:border-0 hover:bg-gray-50 md:p-0 md:hover:bg-transparent md:hover:text-#8c7851"
              >
                About
              </router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </div>
</template>

<style>
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

::-webkit-scrollbar {
  width: 5px; /* for vertical scrollbar */
  height: 5px; /* for horizontal scrollbar */
}

::-webkit-scrollbar-track {
  background: hsl(240, 1%, 17%);
  border-radius: 5px;
}

::-webkit-scrollbar-thumb {
  background: #ffdb70;
  border-radius: 5px;
}

::-webkit-scrollbar-button { width: 20px; }

body {
  font-family: 'Poppins', sans-serif;
  background: hsl(0, 0%, 7%);
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100vh;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
  transition: color 0.3s;
}

nav a.router-link-exact-active {
  display: inline-flex;
  flex-direction: column;
  color: white;
  transition: color 0.3s;
}

nav a.router-link-exact-active::after {
  display: inline-block;
  content: "";
  /* margin-top: 0.08em; */
  width: 100%;
  height: 4px;
  border-radius: 2px;
  background-color: #ffdb70;
}

nav a.router-link-exact-active:hover {
  color: white;
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
</style>
