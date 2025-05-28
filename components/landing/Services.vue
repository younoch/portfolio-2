<template>
  <section class="flex flex-col justify-center bg-none text-[#111] bg-[#f2f2f2] relative ">
    <div
      class="bg-[position:50%_50%] mb-5 h-auto mt-0 text-[#111] bg-[#f2f2f2] text-left relative flex max-w-6xl mx-auto "
    >
      <div class="p-0 relative flex-1 max-w-full">
        <!-- Heading -->
        <h1
          class="font-bold text-3xl sm:text-5xl mx-auto mt-5 sm:mt-11 mb-0 font-roboto break-words relative text-center text-[#111] p-0  "
        >
          Our Services
        </h1>

        <!-- Services Grid -->
        <div class="mx-auto mt-4 sm:mt-8 relative  ">
          <div class="">
            <div class="grid grid-cols-3 gap-4">
              <div
                v-for="(service, index) in services"
                :key="index"
                class="col-span-3 sm:col-span-1"
              >
                <div
                  class="text-[#111] bg-white rounded-3xl text-center relative flex bg-clip-padding bg-origin-padding max-w-full border-solid border-transparent"
                >
                  <div class="rounded-3xl relative flex-1 max-w-full">
                    <span
                      class="mx-auto block text-[#478ac9] text-center relative"
                    >
                      <img
                        :src="service.image"
                        alt=""
                        class="object-contain block w-full h-24 border-none"
                      />
                    </span>
                    <h4
                      class="mx-3 mt-3 mb-0 font-normal text-lg sm:text-2xl font-roboto break-words relative text-[#111] p-0"
                    >
                      <b class="font-bold">{{ service.title }}</b>
                    </h4>
                    <p
                      class="text-base font-normal mx-3 mt-5 sm:mt-8 mb-0 font-roboto break-words relative p-0"
                    >
                      {{ service.description }}
                    </p>
                    <nuxt-link
                      :to="service.link"
                      class="rounded-3xl font-bold uppercase text-sm tracking-[1px] mt-8 mx-auto mb-0 bg-[#adf6f2] text-[#111] table cursor-pointer font-['Open_Sans'] py-3 px-6 self-start transition-[background-color,color,border-color]"
                    >
                      Read More
                    </nuxt-link>
                  </div>
                </div>
              </div> 
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const services = [
  {
    title: 'SAP Services',
    description: 'Expert SAP advisory, implementation, migration, custom development, and Application maintenance service ensure seamless integration, boosting your business efficiency and success',
    image: 'https://scsl.scsl.ltd/global/images/1.png',
    link: '#'
  },
  {
    title: 'IT Staff Augmentation ',
    description: 'Access skilled IT professionals on demand through our IT staff augmentation service. Whether for projects and continuous support, we help business to scale up their team with the skills they need.',
    image: 'https://scsl.scsl.ltd/global/images/21-83c79cbd.png',
    link: '#'
  },
  {
    title: 'Others Services',
    description: 'Our Other Services are Development Services, Managed services, AI & ML, Cyber Security, Training, Cloud Services, CAD Services, GIS Services',
    image: '	https://scsl.scsl.ltd/global/images/4289960-02f4311f.png',
    link: '#'
  },
];
</script>