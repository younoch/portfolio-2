<template>
  <section class="bg-[position:50%_50%] h-fit bg-no-repeat bg-cover relative   block  ">
    <div class="overflow-hidden left-0 top-0 w-full h-full min-h-screen absolute  ">
      <div class="pointer-events-none w-full h-full relative block p-0 overflow-hidden  ">
        <video data-autoplay="1" loop muted autoplay playsinline
          class="object-cover absolute top-0 left-0 bottom-0 h-full w-full border-0 border-none border-[#111]   block">
          <source src="https://scsl.scsl.ltd/global/files/scsl_banner_vid.mp4" type="video/mp4" class=" " />
          <p class="text-lg mt-5 mb-5 p-0  ">Your browser does not support HTML5 video.</p>
        </video>
      </div>
      <div class="absolute inset-0 pointer-events-none  "></div>
    </div>
    <div class="pointer-events-none relative   px-2 sm:px-0">
      <div class="mb-0 pointer-events-auto w-full !important relative   max-w-6xl mx-auto">
        <div class=" ">
          <div class="grid grid-cols-3 gap-2 items-center   pt-16 sm:pt-20">

            <div class="col-span-3 sm:col-span-2 relative flex bg-clip-padding bg-origin-padding">

              <div class="px-0 relative flex-1 max-w-full  ">

                <h1
                  class="will-change-transform mb-0 font-normal text-2xl sm:text-4xl text-white font-roboto animate-fill-both break-words relative sm:text-left p-0   text-center">
                  <b class="  font-bold">Helping Businesses Grow With Cutting-Edge IT Solutions And Expert
                    Resources</b>
                </h1>

                <p
                  class="text-lg sm:text-2xl mt-2 mb-0 text-white break-words relative text-left p-0 table self-start  ">
                  Your Trusted Technology Partner for IT Growth, Digital Transformation & Engineering Precision
                  suggest something formal and shorter.
                </p>
                <div class="flex justify-center sm:justify-start">
                  <a
                    class="border-solid uppercase rounded-3xl text-sm sm:text-lg font-bold mt-[21px] mb-0 px-6 py-2 bg-[#adf6f2] text-black font-roboto no-underline relative table cursor-pointer outline-0 whitespace-nowrap self-start   border-2 transition-[background-color,color,border-color]">
                    Get IN Touch
                  </a>
                </div>
              </div>
            </div>
            <div class="col-span-3 sm:col-span-1 text-left relative flex bg-clip-padding bg-origin-padding">
              <div class="rounded-lg sm:rounded-3xl text-center bg-white pt-4 pb-3 px-3 w-full">
                <h4
                  class="text-lg sm:text-[20px] font-bold mb-0 font-roboto break-words relative text-[#111] p-0 table self-start mx-auto  ">
                  Let's Connect To Help You And Your Team
                </h4>
                <div class="mx-auto relative   text-sm sm:text-base">
                  <form action="https://forms.nicepagesrv.com/v2/form/process" source="email" name="form"
                    class="pr-2 w-[calc(100%_+_10px)] flex flex-wrap items-end  ">

                    <!-- Name Field -->
                    <div class="mx-auto mb-2 sm:mb-3 text-start w-full">
                      <label for="name-8412" class="font-bold   block mb-1">Your Name</label>
                      <input type="text" placeholder="Your Name" name="name" required
                        class="rounded-[15px] border-2 border-[#b3b3b3] bg-white text-black border-solid block w-full px-3 py-2 sm:px-2 sm:py-1.5 outline-0 font-['Open_Sans'] text-[14px] sm:text-base m-0   transition-[border-color,box-shadow] duration-150 ease-in-out" />
                    </div>

                    <!-- Email Field -->
                    <div class="mx-auto mb-2 sm:mb-3 text-start w-full">
                      <label for="email-8412" class="font-bold   block mb-1">Your Work Mail</label>
                      <input type="email" placeholder="Your Work Mail" name="email" required
                        class="rounded-[15px] border-2 border-[#b3b3b3] bg-white text-black border-solid block w-full px-3 py-2 sm:px-2 sm:py-1.5 outline-0 font-['Open_Sans'] text-[14px] sm:text-base m-0   transition-[border-color,box-shadow] duration-150 ease-in-out" />
                    </div>

                    <!-- Message Field -->
                    <div class="mx-auto mb-2 sm:mb-3 text-start w-full">
                      <label for="message-8412" class="font-bold   block mb-1">How Can We Help</label>
                      <textarea placeholder="Tell Us How Can We Help." rows="3" cols="50" name="message" required
                        class="rounded-[15px] border-2 border-[#b3b3b3] bg-white text-black border-solid block w-full px-3 py-2 sm:px-2 sm:py-1.5 outline-0 font-['Open_Sans'] text-[14px] sm:text-base m-0   transition-[border-color,box-shadow] duration-150 ease-in-out min-h-[100px]"></textarea>
                    </div>

                    <!-- Submit Button -->
                    <div class="w-full   mt-1">
                      <UButton
                        class="transition-colors duration-300 bg-cyan-300 hover:bg-cyan-400 uppercase font-bold text-sm sm:text-base md:text-lg text-gray-900 py-2 sm:py-1.5"
                        block label="Submit" variant="solid" :ui="{ rounded: 'rounded-lg' }" />
                    </div>

                    <!-- Success/Error Messages -->
                    <div
                      class="  bg-[#62c584] z-[1] hidden absolute bottom-0 left-0 w-full text-center text-white p-[15px] sm:p-5 border-0">
                      Thank you! Your message has been sent.
                    </div>
                    <div
                      class="  bg-[#f95d51] z-[1] hidden absolute bottom-0 left-0 w-full text-center text-white p-[15px] sm:p-5 border-0">
                      Unable to send your message. Please fix errors then try again.
                    </div>

                    <!-- Hidden Fields -->
                    <input type="hidden" value="" name="recaptchaResponse"
                      class="  outline-0 overflow-clip text-[#111] font-['Open_Sans'] text-base m-0" />
                    <input type="hidden" name="formServices" value="f1252ac8-1ee5-4249-9e32-46d4181951c4"
                      class="  outline-0 overflow-clip text-[#111] font-['Open_Sans'] text-base m-0" />
                  </form>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="pb-40 sm:pb-56"></div>
    <div class="absolute bottom-0 -left-3 -right-3 sm:-left-10 sm:-right-10 h-32 sm:h-48 z-10">
      <div class=" h-full relative">
        <div class="h-full curved-top-bg ">
        </div>
        <div class="absolute left-0 right-0 bottom-1/3 z-20 mx-3 sm:mx-10">
          <h2 class="sm:text-4xl font-bold text-black font-roboto text-center">
            Comprehensive Technology Solutions for Business In Dallas
          </h2>
        </div>
      </div>
    </div>
  </section>

</template>

<script>

</script>

<style lang="scss">
.curved-top-bg {
  background: white;
  border-top-left-radius: 100% 30vw;
  border-top-right-radius: 100% 30vw;
}
</style>