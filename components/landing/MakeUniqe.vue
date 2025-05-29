<template>
  <section class="bg-gradient-to-b from-white to-[#01080c] text-[#111] text-left relative box-border block bg-[position:50%_50%] bg-no-repeat bg-cover">
    <div class=" flex justify-center flex-col  pointer-events-none relative max-w-6xl mx-auto ">
      <h2 class="mt-[2px] text-center sm:text-left font-bold text-4xl sm:text-5xl  mb-0  text-[#111] p-0 pointer-events-auto table self-start w-fit">
        What Makes Us Unique
      </h2>
      
      <div class="mt-[55px] mb-[60px] flex flex-col pointer-events-auto mx-0 w-full relative box-border">
        <div class="min-h-[286px] grid grid-cols-2 gap-2">
          <!-- Feature Cards -->
          <div 
            v-for="(feature, index) in features" 
            :key="index"
            class="bg-none rounded-[10px] text-[#111] bg-white flex relative text-left col-span-2 sm:col-span-1"
          >
            <div class="py-3 px-4 sm:py-5 sm:px-7 rounded-[10px] relative flex-1 max-w-full flex justify-center items-center">
              <span class="h-12 w-12 md:h-16 md:w-16 bg-none my-0 ml-0 text-white bg-[#adf6f2] rounded-full block leading-[0px] border-0 relative box-border">
                <img 
                  src="/images/1828743-ed89434a.png" 
                  alt="" 
                  class="object-contain block w-full h-4 md:h-7 box-border border-none" 
                />
              </span>
              
              <h5 class="mt-[20px] mx-0 normal-case tracking-normal font-bold text-[20px] leading-[24px] mb-0 font-georgia break-words relative text-[#111] p-0 box-border">
                <b class="box-border font-bold">{{ feature.title }}</b>
              </h5>
              
              <p class="mt-[20px] mx-0 not-italic text-[18px] mb-0 leading-[28.8px] break-words relative p-0 box-border">
                {{ feature.description }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const features = [
  {
    title: "Tailored Solutions",
    description: "We provide custom solutions to our customers that align seamlessly with their organizational objectives."
  },
  {
    title: "Commitment to Success",
    description: "We are dedicated to ongoing upgrades for your industry's success, prioritizing every project we take on."
  },
  {
    title: "Our Domain Expertise",
    description: "Our experienced team specializes in implementing IT solutions across various industries."
  },
  {
    title: "Faster Delivery",
    description: "Our team adheres to a clear roadmap to ensure timely product launches, optimizing the delivery cycle wherever possible."
  }
]
</script>