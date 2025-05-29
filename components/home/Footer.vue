<template>
  <footer class="relative overflow-hidden flex justify-center border-t-2 border-gray-400">
    <div
      class="w-full grid md:grid-cols-[140px_1fr] md:pt-[3.75rem] lg:grid-cols-[142px_752px_1fr] lg:pt-0 lg:max-w-7xl lg:after:absolute lg:after:inset-0 lg:after:left-[calc(50%+630px)] lg:after:bg-gray-50 lg:after:content-[&quot;&quot;]"
    >
      <div
        class="px-10 py-6 md:py-0 md:row-[1] md:float-left lg:pt-16 lg:row-span-3 lg:col-start-1 lg:row-start-1"
      >
        <img
          alt="SLSC Logo"
          loading="lazy"
          width="100"
          height="auto"
          decoding="async"
          data-nimg="1"
          style="color: transparent"
          src="/images/scsl308.webp"
        />
      </div>
      
      <section
        class="grid w-full grid-cols-1 px-10 md:grid-cols-3 md:pl-0 md:px-0 md:gap-4 md:grid-cols-[1fr_1fr_0.8fr] md:row-[1] md:col-span-2 mdL:col-span-3 lg:row-span-3 lg:pt-16 lg:row-start-1 lg:col-start-2 lg:col-span-1"
      >
        <div 
          v-for="(section, index) in navigationSections" 
          :key="index"
          class="mb-8 md:max-w-[12.25rem]"
        >
          <ul>
            <li class="text-xl font-bold mb-4 lg:mb-6">
              <template v-if="section.link">
                <a :href="section.link">
                  <strong>{{ section.title }}<span class="text-amber-600">.</span></strong>
                </a>
              </template>
              <template v-else>
                <strong>{{ section.title }}<span class="text-amber-600">.</span></strong>
              </template>
            </li>
            <li
              v-for="(item, itemIndex) in section.items"
              :key="itemIndex"
              class="text-sm mb-3 text-gray-900 hover:underline"
            >
              <a :href="item.link" class="">{{ item.text }}</a>
            </li>
          </ul>
        </div>
      </section>
      
      <section
        class="w-full bg-gray-50 px-10 row-[5] md:row-start-4 md:col-span-2 mdL:p-10 mdL:col-span-3 lg:row-start-1 lg:pb-0 lg:pt-16 lg:pl-7 lg:pl-10 lg:pr-0 lg:col-span-1"
      >
        <p class="text-xl font-bold mb-6">
          Get in touch<span class="text-amber-600">.</span>
        </p>
        <div
          class="float-left grid grid-cols-[_auto,_auto] gap-x-2 gap-y-5 md:[&amp;_a:first-child]:col-start-2 [&amp;_a:last-of-type]:col-start-1 [&amp;_a:last-of-type]:row-start-1"
        >
          <a
            rel="noreferrer"
            target="_blank"
            class="w-fit flex items-center justify-center gap-2 disabled:pointer-events-none [&amp;_svg]:fill-current outline-none px-4 rounded-lg active:shadow-none disabled:bg-gray-200 disabled:text-gray-50 bg-amber-600 hover:bg-amber-700 hover:text-white active:bg-amber-800 active:text-white text-white focus:text-white focus:shadow-amber-50 py-3 text-xl font-medium col-span-2 md:col-span-1 h-11"
            href="/">
            <span class="">Schedule a Call</span><span class="">
              <UIcon name="i-mdi:arrow-right-thin" />
            </span>
          </a>
          <a
            rel="noreferrer"
            class="w-fit flex items-center justify-center gap-2 disabled:pointer-events-none [&amp;_svg]:fill-current outline-none px-4 border-2 rounded-lg box-border bg-transparent text-gray-900 active:shadow-none hover:text-white disabled:bg-gray-200 disabled:border-gray-200 disabled:text-gray-50 border-current hover:bg-gray-900 hover:border-gray-900 focus:shadow-amber-50 py-3 text-xl font-medium col-span-2 md:col-span-1 h-11"
            href="/contact">
            <span class="">Contact Us</span>
          </a>
          <div
            class="flex items-center text-base col-span-2 transition-all hover:text-primary-600"
          >
              <UIcon name="i-mdi:phone" class="w-4 h-4 mr-2 bg-gray-900"/>
            <a href="tel:+14084782739">+1 (234) 567-8910</a>
          </div>
          <div
            class="flex items-center text-base col-span-2 transition-all hover:text-primary-600"
          >
              <UIcon name="i-mdi:mail-ru" class="w-4 h-4 mr-2 bg-gray-900"/>
            <a href="mailto:info@stargroup-bd.com">info@stargroup-bd.com</a>
          </div>
          <div
            class="flex items-center text-base col-span-2 transition-all hover:text-primary-600"
          >
              <UIcon name="i-mdi:map-marker-radius" class="w-5 h-5 mr-2 bg-gray-900"/>
            <span>Fattah Plaza(7th floor) <br> 70 Green Road Dhaka 1205,<br> Bangladesh</span>
          </div>
        </div>
      </section>
      
      <!-- <section class="bg-gray-50 p-10 pb-8 w-full md:row-start-3 md:col-span-2 mdL:col-span-1 mdL:row-start-4 mdL:w-[50vw] lg:row-start-2 lg:col-span-1 lg:py-14 lg:pl-7 lg:w-full lg:py-11 lg:pl-10 lg:pr-0">
        <p class="font-bold max-w-sm text-base mb-4">
          Get insights from the experts on building and scaling technology
          teams.
        </p>
        <div class="max-w-xl items-center justify-center">
          <div
            class="mx-auto mt-6 flex-col items-center justify-center text-center text-base hidden"
          >
            <div class="items-center justify-center text-center">
              
            </div>
            <br /><span class="text-white"> Sending information... </span>
          </div>
          <div class="">
            <div></div>
            <form
              id=""
              class="grid float-left gap-y-3 md:gap-x-3 md:gap-y-2 md:grid-cols-2 md:float-none md:grid-cols-2 md:gap-x-4"
              data-gtm-vis-first-on-screen6527105_182="301"
              data-gtm-vis-total-visible-time6527105_182="100"
              data-gtm-vis-has-fired6527105_182="1"
            >
              <div>
                <div
                  class="flex flex-col flex-wrap gap-1 relative 2xl:!flex-row [&amp;>label]:w-full"
                >
                  <label for=":Rbajlida:" class="flex flex-col gap-1"
                    ><div
                      id="label-top-:Rbajlida:"
                      class="label text-gray-600 text-base"
                    >
                      Your e-mail address
                    </div>
                    <div
                      class="[&amp;_input]:w-full group relative flex outline outline-1 items-center rounded-[4px] flex-nowrap outline-offset-[-1px] cursor-default outline-gray-100 hover:outline-gray-400 focus-within:outline-gray-600 focus-within:hover:outline-gray-600 focus-within:!shadow-amber-50 [&amp;:not(:focus-within)]:outline-gray-100 [&amp;:not(:focus-within)]:outline-1 focus-within:outline-1 focus-within:-outline-offset-1 focus-within:shadow-ring gap-2 px-2 py-2 [&amp;_input]:text-base [&amp;_textarea]:text-base text-gray-900 bg-white [&amp;_input]:bg-white [&amp;_input]:placeholder:text-gray-400 [&amp;_textarea]:bg-white [&amp;_textarea]:placeholder:text-gray-400"
                      id="label-field-:Rbajlida:"
                    >
                      <div class="flex flex-1 flex-col flex-wrap leading-5">
                        <input
                          class="border-none focus:outline-none"
                          type="email"
                          aria-label="email"
                          id=":Rbajlida:"
                          maxlength="140"
                          placeholder="name@email.com"
                          name="email"
                          value=""
                        />
                      </div></div
                  ></label>
                </div>
              </div>
              <div class="relative row-[3] md:col-span-full md:row-[2]">
                <fieldset class="flex flex-wrap">
                  <legend class="hidden">Accept</legend>
                  <input
                    id=":R5ajlida:"
                    type="checkbox"
                    class="opacity-0 w-0 h-0 [&amp;:checked~label>div_svg]:visible [&amp;:checked~label>div]:bg-gray-900 [&amp;:checked~label>div]:border-gray-900"
                    name="understoodTerms"
                    value=""
                  /><label
                    for=":R5ajlida:"
                    class="flex items-center gap-3 cursor-pointer"
                    ><div
                      class="flex items-center justify-center w-[1.125rem] h-[1.125rem] rounded-sm border-2 border-solid border-neutrals-700 hover:ring hover:ring-offset-2 hover:ring-amber-50 hover:ring-offset-amber-50"
                    >
                      <span class=""
                        ></span>
                    </div>
                    <span
                      class="text-neutrals-700 text-[1.05rem] leading-6 font-medium"
                    >
                      <span class="text-xs"
                        >By subscribing I accept the
                        <a
                          href="https://www.bairesdev.com/privacy-policy/"
                          target="_blank"
                          class="terms-link underline"
                          rel="noreferrer noopener"
                          >Privacy Policy</a
                        >.</span
                      >
                    </span></label
                  >
                </fieldset>
              </div>
              <button
                type="submit"
                class="flex items-center justify-center gap-2 disabled:pointer-events-none [&amp;_svg]:fill-current outline-none px-4 border-2 rounded-lg box-border bg-transparent text-gray-900 active:shadow-none hover:text-white disabled:bg-gray-200 disabled:border-gray-200 disabled:text-gray-50 border-current hover:bg-gray-900 hover:border-gray-900 focus:shadow-amber-50 py-2.5 text-base font-medium h-11 w-[140px] xl:ml-2 text-sm md:mt-6"
              >
                <span class="">Subscribe</span>
                <span class=""></span>
              </button>
            </form>
          </div>
        </div>
      </section> -->
      
      <section
        class="bg-gray-50 p-10 w-full md:row-start-5 md:col-span-2 md:px-10 md:pb-10 md:pt-0 mdL:col-span-4 lg:row-start-3 lg:row-span-2 lg:col-span-1 lg:pl-7 lg:pl-10"
      >
        <p class="text-xl mb-4 font-bold">
          Follow us<span class="text-amber-600">.</span>
        </p>
        <ul class="flex gap-4">
          <li 
            v-for="social in socialLinks" 
            :key="social.name"
            class="text-white"
          >
            <a
              :aria-label="social.name"
              :href="social.link"
              target="_blank"
              rel="noreferrer"
              class="flex h-8 w-8 items-center justify-center transition-all duration-500 [&amp;_svg]:fill-gray-700 [&amp;:hover_svg]:fill-amber-600"
            >
              <UIcon :name="social.icon" />
            </a>
          </li>
        </ul>
      </section>
      
      <div class="hidden"></div>
      
      <section
        class="flex flex-col row-start-3 p-10 pt-2 md:row-start-2 md:col-start-2 md:p-0 md:px-0 md:row-start-2 md:col-start-2 md:col-span-2 mdL:row-start-2 mdL:col-start-2 mdL:col-span-2 lg:row-start-4 lg:col-start-2 lg:col-span-1"
      >
        <div class="text-xs mb-6">
          <template v-for="(link, index) in footerLinks" :key="index">
            <a
              :href="link.url"
              target="_blank"
              rel="noreferrer"
              class="hover:underline"
            >{{ link.text }}</a>
            <span v-if="index < footerLinks.length - 1" class="mx-2">|</span>
          </template>
        </div>
        <div class="mb-8 md:mb-6 lg:mb-16 text-xs">
          <p>
            SLSC 2009 - {{ currentYear }}. All rights reserved.
          </p>
        </div>
      </section>
    </div>
  </footer>
</template>

<script setup lang="ts">
import { UIcon } from '#components';

const currentYear = new Date().getFullYear();

const navigationSections = [
  {
    title: 'Discover SCSL',
    link: '',
    items: [
      { text: 'About Us', link: '/' },
      { text: 'Managed Service', link: '/' },
    ]
  },
  {
    title: 'Resources',
    link: '',
    items: [
      { text: 'Blog', link: '/' },
      { text: 'ML & AI', link: '/' },
    ]
  },
  {
    title: 'Careers',
    link: '/',
    items: [
      { text: 'Job Opportunities', link: '/' },
    ]
  }
];

const socialLinks = [
  { name: 'Linkedin', link: '/', icon: 'i-mdi:linkedin' },
  { name: 'Facebook', link: '', icon: 'i-mdi:facebook' },
  { name: 'X', link: '', icon: 'i-mdi:twitter' },
  { name: 'Instagram', link: '/', icon: 'i-mdi:instagram' },
  { name: 'Youtube', link: '/', icon: 'i-mdi:youtube' }
];

const footerLinks = [
  { text: 'Privacy Policy', url: '/' },
  { text: 'Terms of Service', url: '/' },
  { text: 'Do Not Sell My Personal Information', url: '/' }
];
</script>

<style scoped lang="scss"></style>