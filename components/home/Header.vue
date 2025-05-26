<template>
  <header
    class="transition-all duration-300 ease-[cubic-bezier(0.4,0,0.2,1)] shadow-[rgba(0,0,0,0)_0px_0px_0px_0px,rgba(0,0,0,0)_0px_0px_0px_0px,rgba(0,0,0,0.05)_0px_1px_2px_0px] py-4 w-full z-50 top-0 fixed border-0 border-solid border-[rgb(229,231,235)] box-border"
    :class="{'bg-white shadow-md': scrolled, 'bg-transparent': !scrolled}"
  >
    <div class="max-w-6xl mx-auto w-full border-0 border-solid border-[rgb(229,231,235)] box-border">
      <nav class="px-1 flex justify-between items-center border-0 border-solid border-[rgb(229,231,235)] box-border">
        <nuxt-link
          to="/"
          class="text-sky-800 font-bold text-lg md:text-2xl leading-8 relative no-underline border-0 border-solid border-[rgb(229,231,235)] box-border"
        >
          <img 
            src="https://scsl.scsl.ltd/global/images/scsl308.webp" 
            alt="Company Logo"
            class="h-8 md:h-12 transition-all duration-300"
          >
        </nuxt-link>
        
        <!-- Desktop Navigation -->
        <ul class="hidden md:flex gap-8 list-none m-0 p-0 border-0 border-solid border-[rgb(229,231,235)] box-border">
          <li
            v-for="(item, index) in routesHeader"
            class="border-0 border-solid border-[rgb(229,231,235)] box-border relative group flex justify-center items-center"
            :key="index"
          >
            <template v-if="!item.children">
              <nuxt-link
                :to="item.path"
                class="relative transition-all duration-300 ease-[cubic-bezier(0.4,0,0.2,1)] uppercase font-bold py-2 no-underline border-0 border-solid border-[rgb(229,231,235)] box-border text-lg"
                :class="currentRoute === item.path ? 'text-sky-600' : 'text-gray-600'"
              >
                {{ item.name }}
              </nuxt-link>
            </template>
            <template v-else>
              <div class="relative">
                <button
                  class="relative transition-all duration-300 ease-[cubic-bezier(0.4,0,0.2,1)] uppercase font-bold py-2 no-underline border-0 border-solid border-[rgb(229,231,235)] box-border text-lg flex items-center gap-1"
                  :class="currentRoute === item.path ? 'text-sky-600' : 'text-gray-600'"
                >
                  {{ item.name }}
                  <span class="i-uil:angle-down text-base transition-transform duration-200 group-hover:rotate-180"></span>
                </button>
                <ul
                  class="absolute left-0 top-full mt-0 w-56 bg-white rounded-md shadow-lg py-2 z-50 opacity-0 invisible group-hover:opacity-100 group-hover:visible transition-all duration-200 origin-top"
                >
                  <li v-for="(child, childIndex) in item.children" :key="childIndex" class="px-4 py-2 hover:bg-gray-50">
                    <nuxt-link
                      :to="child.path"
                      class="block text-gray-800 hover:text-sky-800 transition-colors"
                    >
                      {{ child.name }}
                    </nuxt-link>
                  </li>
                </ul>
              </div>
            </template>
          </li>
        </ul>
        
        <!-- Mobile Menu Button -->
        <button
          class="md:hidden text-gray-800 text-2xl"
          @click="toggleMenuHandler"
        >
          <span :class="iconClass"></span>
        </button>
      </nav>
      
      <!-- Mobile Navigation -->
      <nav v-if="toggleMenu" class="md:hidden mt-4 pb-2">
        <div class="flex flex-col">
          <template v-for="(item, index) in routesHeader" :key="index">
            <template v-if="!item.children">
              <nuxt-link
                class="py-2 px-4 rounded-md transition-colors text-center font-medium"
                :to="item.path"
                :class="currentRoute === item.path ? 'text-sky-800 bg-gray-200' : 'text-gray-800'"
              >
                {{ item.name }}
              </nuxt-link>
            </template>
            <template v-else>
              <button
                class="py-2 px-4 rounded-md transition-colors text-center font-medium flex items-center justify-center gap-1"
                :class="currentRoute === item.path ? 'text-sky-800 bg-gray-200' : 'text-gray-800'"
                @click="toggleServicesMenu"
              >
                {{ item.name }}
                <span class="i-uil:angle-down text-base transition-transform duration-200" :class="{'rotate-180': showServicesMenu}"></span>
              </button>
              <div v-if="showServicesMenu" class="pl-4">
                <nuxt-link
                  v-for="(child, childIndex) in item.children"
                  :key="childIndex"
                  :to="child.path"
                  class="block py-2 px-4 rounded-md transition-colors text-center font-medium text-gray-800 hover:bg-gray-100"
                >
                  {{ child.name }}
                </nuxt-link>
              </div>
            </template>
          </template>
        </div>
      </nav>
    </div>
  </header>
</template>

<script setup lang="ts">
const routesHeader = [
  { name: "Home", path: "/" },
  { name: "About", path: "/about" },
  { 
    name: "Services",
    children: [
      { name: "Sav Services", path: "/sav-services" },
      { name: "IT Staff Augmentation", path: "/it-staff" },
      { name: "Other Services", path: "/other-services" },
    ]
  },
  { name: "Contact Us", path: "/contact" },
];

const route = useRoute();
const toggleMenu = ref(false);
const showServicesMenu = ref(false);

const toggleMenuHandler = () => {
  toggleMenu.value = !toggleMenu.value;
  if (!toggleMenu.value) {
    showServicesMenu.value = false;
  }
};

const toggleServicesMenu = () => {
  showServicesMenu.value = !showServicesMenu.value;
};

const currentRoute = computed(() => {
  return route.path;
});
const iconClass = computed(() => (toggleMenu.value ? 'i-uil:times' : 'i-uil:apps'));

const scrolled = ref(false);
const handleScroll = () => {
  scrolled.value = window.scrollY > 10;
};

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onBeforeUnmount(() => {
  window.removeEventListener('scroll', handleScroll);
});
</script> 