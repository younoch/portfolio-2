<template>
  <footer class="relative overflow-hidden flex justify-center">
    <div
      class="w-full grid md:grid-cols-[140px_1fr] md:pt-[3.75rem] lg:grid-cols-[142px_752px_1fr] lg:pt-0 lg:max-w-7xl lg:after:absolute lg:after:inset-0 lg:after:left-[calc(50%+630px)] lg:after:bg-gray-50 lg:after:content-['']">
      <!-- Logo Section -->
      <div class="px-10 py-6 md:py-0 md:row-[1] md:float-left lg:pt-16 lg:row-span-3 lg:col-start-1 lg:row-start-1">
        <img alt="SLSL Logo" loading="lazy" width="60" height="40" decoding="async" style="color:transparent"
          src="/images/scsl308.webp">
      </div>

      <!-- Main Links Section -->
      <section
        class="grid w-full grid-cols-1 px-10 md:grid-cols-3 md:pl-0 md:px-0 md:gap-4 md:grid-cols-[1fr_1fr_0.8fr] md:row-[1] md:col-span-2 lg:col-span-3 lg:row-span-3 lg:pt-16 lg:row-start-1 lg:col-start-2 lg:col-span-1">
        <!-- Discover BairesDev -->
        <div class="mb-8 md:max-w-[12.25rem]">
          <ul>
            <li class="text-xl font-bold mb-4 lg:mb-6">
              <strong>Discover SLSL<span class="text-primary-600">.</span></strong>
            </li>
            <li class="text-sm mb-3 text-gray-900 hover:underline">
              <a href="/about">About Us</a>
            </li>
            <!-- More list items... -->
          </ul>
        </div>

        <!-- Resources -->
        <div class="mb-8 md:max-w-[12.25rem]">
          <ul>
            <li class="text-xl font-bold mb-4 lg:mb-6">
              <strong>Resources<span class="text-primary-600">.</span></strong>
            </li>
            <li class="text-sm mb-3 text-gray-900 hover:underline">
              <a href="/clients">Case Studies</a>
            </li>
            <!-- More list items... -->
          </ul>
        </div>

        <!-- Careers -->
        <div class="mb-8 md:max-w-[12.25rem]">
          <ul>
            <li class="text-xl font-bold mb-4 lg:mb-6">
              <a href="/join-us">Careers<span class="text-primary-600">.</span></a>
            </li>
            <li class="text-sm mb-3 text-gray-900 hover:underline">
              <a href="https://talent.bairesdev.com/">Job Opportunities</a>
            </li>
            <!-- More list items... -->
          </ul>
        </div>
      </section>

      <!-- Get in Touch Section -->
      <section
        class="w-full bg-gray-50 px-10 row-[5] md:row-start-4 md:col-span-2 lg:p-10 lg:col-span-3 lg:row-start-1 lg:pb-0 lg:pt-16 lg:pl-7 lg:pr-0 lg:col-span-1">
        <p class="text-xl font-bold mb-6">Get in touch<span class="text-primary-600">.</span></p>
        <div
          class="float-left grid grid-cols-[auto,auto] gap-x-2 gap-y-5 md:[&_a:first-child]:col-start-2 [&_a:last-of-type]:col-start-1 [&_a:last-of-type]:row-start-1">
          <a href="https://www.bairesdev.com/start/basic-details/"
            class="w-fit flex items-center justify-center gap-2 px-4 rounded-lg bg-primary-600 hover:bg-primary-700 text-white py-3 text-xl font-medium col-span-2 md:col-span-1 h-11">
            <span>Schedule a Call</span>
            <svg class="transition-colors duration-300" width="20" height="20" viewBox="0 0 16 9" fill="none"
              xmlns="http://www.w3.org/2000/svg">
              <!-- SVG path... -->
            </svg>
          </a>
          <!-- More buttons... -->
        </div>
      </section>

      <!-- Newsletter Section -->
      <section
        class="bg-gray-50 p-10 pb-8 w-full md:row-start-3 md:col-span-2 lg:col-span-1 lg:row-start-4 lg:py-14 lg:pl-7 lg:w-full">
        <p class="font-bold max-w-sm text-base mb-4">Get insights from the experts on building and scaling technology
          teams.</p>
        <!-- Newsletter form... -->
      </section>

      <!-- Social Media Section -->
      <section
        class="bg-gray-50 p-10 w-full md:row-start-5 md:col-span-2 lg:px-10 lg:pb-10 lg:pt-0 lg:col-span-4 lg:row-start-3 lg:row-span-2 lg:col-span-1 lg:pl-7 lg:pl-10">
        <p class="text-xl mb-4 font-bold">Follow us<span class="text-primary-600">.</span></p>
        <ul class="flex gap-4">
          <li>
            <a aria-label="Linkedin" href="https://www.linkedin.com/company/bairesdev"
              class="flex h-8 w-8 items-center justify-center transition-all duration-500">
              <svg class="h-4 w-4 lg:h-6 lg:w-6" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                <!-- SVG path... -->
              </svg>
            </a>
          </li>
          <!-- More social icons... -->
        </ul>
      </section>

      <!-- Footer Links -->
      <section
        class="flex flex-col row-start-3 p-10 pt-2 md:row-start-2 md:col-start-2 md:p-0 md:px-0 lg:row-start-4 lg:col-start-2 lg:col-span-1">
        <div class="text-xs mb-6">
          <a href="https://www.bairesdev.com/privacy-policy/" class="hover:underline">Privacy Policy</a>
          <span class="mx-2">|</span>
          <a href="https://www.bairesdev.com/terms-conditions/" class="hover:underline">Terms of Service</a>
          <span class="mx-2">|</span>
          <a href="https://www.bairesdev.com/do-not-sell-my-personal-information/" class="hover:underline">Do Not Sell
            My Personal Information</a>
        </div>
        <div class="mb-8 md:mb-6 lg:mb-16 text-xs">
          <p>SLSL 2009 - 2025. All rights reserved.</p>
        </div>
      </section>
    </div>
  </footer>
</template>

<script setup lang="ts">

const state = ref<any>('');

</script>

<style scoped lang="scss"></style>