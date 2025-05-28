<template>
  <section class="bg-none text-[#111] bg-white text-center relative max-w-6xl mx-auto  block px-4 sm:px-6 lg:px-8">
    <div class="w-full pointer-events-none relative mx-auto  ">
      
      <h2
        class=" mt-8 md:mt-16 mx-auto mb-0 font-bold text-3xl md:text-4xl font-roboto break-words relative text-center text-[#111] p-0 pointer-events-auto table self-start w-fit">
        We Are SCSL
      </h2>
      <div class="grid grid-cols-2 mt-8 md:mt-14 gap-4 sm:gap-6">
        <div class="ml-0 md:ml-5 pointer-events-auto relative col-span-2 sm:col-span-1">
          <div class="sm:p-4 relative grid grid-cols-2 gap-4 md:gap-12">
            <div class=" md:block left-1/2 h-full absolute md:border-l-[3px] border-solid border-gray-500 pointer-events-auto  "></div>
            <div class=" md:block top-1/2 w-full absolute md:border-t-[3px] border-solid border-gray-500 pointer-events-auto  "></div>
            <div v-for="(stat, index) in stats" :key="index"
              class="text-left flex relative  ">
              <div class="p-0 relative flex items-start gap-3 sm:gap-6 max-w-full">
                <span class="w-12 md:w-16 h-12 md:h-16 text-[#478ac9]">
                  <img :src="stat.icon" alt="" class="object-contain w-full h-full border-none" />
                </span>
                <div>
                  <p class="text-2xl md:text-3xl font-bold text-[#478ac9] font-open-sans">
                    {{ stat.value }}
                  </p>
                  <p class="text-sm md:text-base font-normal text-[#111] font-roboto">
                    {{ stat.label }}
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
  
        <div class="px-4 md:px-0 col-span-2 sm:col-span-1">
          <p
            class="w-auto text-sm md:text-base break-words relative text-justify p-0 pointer-events-auto  ">
            Founded in 1998 in Dhaka, Bangladesh, Star Computer Systems Limited (SCSL) has successfully delivered over
            270 projects both locally and internationally. With ISO 27001 certification and CMMI Level 3 appraisal in
            2015, reappraised in 2018, SCSL is a recognized leader in tech-based professional services in the country.
            We specialize in Software Development, IT Staff Augmentation, AI & ML Solutions, cybersecurity Solutions, IT
            Consultancy and Training.
          </p>
          <div class="flex items-center gap-4 justify-center">
            <p
              class="text-center font-bold text-lg md:text-xl break-words relative pointer-events-auto  ">
              ISO 27001:2013 Certified Company
            </p>
    
            <div class="flex justify-center ">
              <img src="https://scsl.scsl.ltd/global/images/iso.webp" alt="" data-image-width="120" data-image-height="120"
                class="w-[90px] h-[90px] md:w-[120px] md:h-[120px] pointer-events-auto object-contain block relative   border-none" />
            </div>
          </div>
  
          <div class="flex justify-center mt-2 sm:mt-4">
            <a href=""
              class="rounded-3xl font-bold uppercase  md:text-lg py-1 md:py-2 px-3 md:px-6 bg-[#adf6f2] text-[#111] no-underline relative cursor-pointer transition-[background-color,color,border-color]">
              CONTINUE
            </a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script setup lang="ts">
  const stats = reactive([
        {
          icon: "https://scsl.scsl.ltd/global/images/10733362-0dac3d7f.png",
          value: "27+",
          label: "Years Of Experience"
        },
        {
          icon: "https://scsl.scsl.ltd/global/images/1322236-25cb8d07.png",
          value: "160+",
          label: "Satisfied Customer"
        },
        {
          icon: "https://scsl.scsl.ltd/global/images/78948-a2607a33.png",
          value: "110+",
          label: "Full Time Technical Resources"
        },
        {
          icon: "https://scsl.scsl.ltd/global/images/3468821-723fa01e.png",
          value: "24/7",
          label: "Support Service"
        }
      ])
</script>

<style></style>