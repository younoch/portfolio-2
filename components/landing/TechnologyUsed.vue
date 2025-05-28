<template>
  <section class="bg-none text-[#111] bg-[#f2f2f2] text-center relative block p-4 sm:p-6 lg:p-8">
    <div class="w-full pointer-events-none relative max-w-6xl mx-auto">
      <h2
        class="mx-auto mb-0 font-bold text-3xl md:text-4xl font-roboto break-words relative text-center text-[#111] p-0 pointer-events-auto table self-start w-fit">
        Technology We Use
      </h2>
      <div>
        <blockquote
          class="mx-auto my-1.5 mb-5 border-l-4 text-lg italic pl-5 py-[10px] pr-5 text-center border-[#478ac9] w-fit">
          Our team has expertise in almost every programming language
        </blockquote>
      </div>
      <div class="relative box-border h-[120px] overflow-hidden space-y-1">
        <div class="h-12 sm:h-16 whitespace-nowrap animate-scroll-left">
          <div class="text-4xl sm:text-5xl font-bold text-[#212525] inline-block">
            Rails &nbsp;&nbsp; Node.js &nbsp;&nbsp; Java &nbsp;&nbsp; React &nbsp;&nbsp; .NET &nbsp;&nbsp; Python &nbsp;&nbsp; C#
          </div>
        </div>
        <div class="h-12 sm:h-16 whitespace-nowrap animate-scroll-right">
          <div class="text-4xl sm:text-5xl font-bold text-[#212525] inline-block">
            Rails &nbsp;&nbsp; Node.js &nbsp;&nbsp; Java &nbsp;&nbsp; React &nbsp;&nbsp; .NET &nbsp;&nbsp; Python &nbsp;&nbsp; C#
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<style>
  @keyframes scroll-left {
    0% {
      transform: translateX(100%);
    }
    100% {
      transform: translateX(-100%);
    }
  }

  @keyframes scroll-right {
    0% {
      transform: translateX(-100%);
    }
    100% {
      transform: translateX(100%);
    }
  }

  .animate-scroll-left {
    animation: scroll-left 15s linear infinite;
  }

  .animate-scroll-right {
    animation: scroll-right 15s linear infinite;
  }
</style>
