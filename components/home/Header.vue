<template>
  <header
    class="pt-3 pb-1 w-full z-50 top-0 fixed border-0 border-solid border-[rgb(229,231,235)]  "
    :class="{ 'bg-white': scrolled, 'bg-transparent': !scrolled }"
  >
    <div class="max-w-6xl mx-auto w-full  ">
      <nav class="px-1 flex justify-between items-center  ">
        <!-- Logo -->
        <nuxt-link to="/" class="text-cyan-800 font-bold text-lg md:text-2xl leading-8 relative no-underline   justify-self-center">
          <img src="https://scsl.scsl.ltd/global/images/scsl308.webp" alt="Company Logo" class="h-8 md:h-12" />
        </nuxt-link>

        <!-- Desktop Navigation -->
        <ul class="hidden md:flex gap-8 list-none m-0 p-0  ">
          <li
            v-for="(item, index) in routesHeader"
            :key="index"
            class="relative flex justify-center items-center group "
          >
            <template v-if="!item.children">
              <nuxt-link
                :to="item.path"
                class="relative uppercase font-bold py-2 no-underline"
                :class="currentRoute === item.path ? 'text-cyan-400' : 'text-gray-400'"
              >
                {{ item.name }}
              </nuxt-link>
            </template>

            <template v-else>
              <div class="relative">
                <!-- Toggle Label -->
                <div
                  class="cursor-pointer relative uppercase font-bold py-2 no-underline flex items-center text-gray-400 group-hover:text-cyan-600"
                >
                  {{ item.name }}
                  <UIcon class="size-6" name="i-mdi:chevron-down" />
                </div>
                <div
                  class="w-full absolute z-10 -bottom-4 flex justify-center opacity-0 invisible group-hover:opacity-100 group-hover:visible transition-all duration-200"
                >
                  <UIcon class="size-10 bg-cyan-400" name="i-mdi:triangle-small-up" />
                </div>

                <!-- Dropdown -->
                <ul
                  class="absolute right-0 top-full mt-0 w-40 bg-cyan-400 rounded-lg shadow-lg pt-1.5 z-50 opacity-0 invisible transform -translate-y-5 scale-y-95
                        group-hover:opacity-100 group-hover:visible group-hover:translate-y-0 group-hover:scale-y-100 transition-all duration-700 ease-[cubic-bezier(0.25, 0.8, 0.25, 1)] origin-top overflow-hidden border border-solid border-cyan-500"
                >
                  <li
                    v-for="(child, childIndex) in item.children"
                    :key="childIndex"
                    class="px-2 py-1 hover:bg-cyan-400 bg-white hover:text-white rounded-sm"
                  >
                    <nuxt-link :to="child.path" class="block w-full no-underline">
                      {{ child.name }}
                    </nuxt-link>
                  </li>
                </ul>
              </div>
            </template>
          </li>
        </ul>

        <!-- Mobile Menu Button -->
        <div class="md:hidden flex items-center">
          <button @click="mobileOpen = !mobileOpen" class="text-cyan-700">
            <UIcon :name="mobileOpen ? 'i-mdi:close' : 'i-mdi:menu'" class="w-8 h-8" />
          </button>
        </div>
      </nav>

      <!-- Mobile Dropdown -->
      <transition name="fade">
        <div
          v-if="mobileOpen"
          class="md:hidden mt-3 px-4 bg-white shadow-lg rounded-lg py-4 space-y-2 transition-all duration-300"
        >
          <div v-for="(item, index) in routesHeader" :key="index">
            <template v-if="!item.children">
              <nuxt-link
                :to="item.path"
                class="block py-2 text-gray-700 font-semibold no-underline"
                @click="mobileOpen = false"
              >
                {{ item.name }}
              </nuxt-link>
            </template>

            <template v-else>
              <div>
                <button
                  @click="toggleSubMenu(index)"
                  class="w-full text-left py-2 font-semibold text-gray-700 flex justify-between items-center"
                >
                  {{ item.name }}
                  <UIcon :name="openSubMenu === index ? 'i-mdi:chevron-up' : 'i-mdi:chevron-down'" class="w-5 h-5" />
                </button>
                <div v-if="openSubMenu === index" class="pl-4">
                  <nuxt-link
                    v-for="(child, childIndex) in item.children"
                    :key="childIndex"
                    :to="child.path"
                    class="block py-1 text-gray-600 no-underline"
                    @click="mobileOpen = false"
                  >
                    {{ child.name }}
                  </nuxt-link>
                </div>
              </div>
            </template>
          </div>
        </div>
      </transition>
    </div>
  </header>
</template>

<script setup>
import { useRoute } from 'vue-router'
import { ref, onMounted } from 'vue'
import { UIcon } from '#components'

const route = useRoute()
const currentRoute = ref(route.path)
const scrolled = ref(false)

onMounted(() => {
  window.addEventListener('scroll', () => {
    scrolled.value = window.scrollY > 10
  })
})

// Sample navigation structure
const routesHeader = [
  { name: 'Home', path: '/' },
  { name: 'About', path: '/about' },
  {
    name: 'Services',
    path: '/services',
    children: [
      { name: 'Design', path: '/services/design' },
      { name: 'Development', path: '/services/development' },
    ],
  },
  { name: 'Contact', path: '/contact' },
]

const mobileOpen = ref(false)
const openSubMenu = ref(null)

const toggleSubMenu = (index) => {
  openSubMenu.value = openSubMenu.value === index ? null : index
}
</script>

<style>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

</style>