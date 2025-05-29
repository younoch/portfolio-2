<template>
  <section class="text-center max-w-6xl mx-auto mt-4 sm:mt-8">
    <div
      class="pointer-events-none relative mx-auto grid grid-cols-3"
    >
      <div class="flex flex-col justify-center col-span-3 sm:col-span-1">
        <h2
          class="text-center sm:text-left text-3xl sm:text-4xl font-bold mb-0  text-[#111] p-0 pointer-events-auto"
        >
          Over 270+ Successful Projects I​n Different Countries&nbsp;&nbsp;
        </h2>
        <a
          href="#"
          class="text-center mt-6 ms:mt-11 ml-0 font-bold uppercase text-base sm:text-lg tracking-[1px] bg-none py-3 sm:py-5 px-4 sm:px-7 pb3 sm:pb-5 bg-[#adf6f2] text-[#111] mb-10 sm:mb-14 border-0 border-transparent rounded-full border-solid no-underline relative box-border transition-[background-color,color,border-color] table select-none align-middle self-center sm:self-start"
        >
          MOre Case Studies
        </a>
      </div>
      <div
        class=" ml-auto flex flex-col pointer-events-auto relative col-span-3 sm:col-span-2"
      >
        <div
          class="grid grid-cols-1 gap-[30px] flex-1"
        >
          <div v-for="(item, index) in cadProjects" :key="index" class="flex relative text-left box-border">
            <div
              class="flex justify-center px-[20px] relative flex-1 max-w-full gap-3 sm:gap-5"
            >
            <div>

              <div class="will-change-transform will-change-opacity p-3 sm:p-4 text-white bg-[#333] rounded-full text-center relative flex "
              >
                <div
                  class="rounded-full flex flex-col justify-center relative flex-1 max-w-full transition-[duration:0s]"
                >
                <div>

                  <h5
                    class="text-2xl sm:text-3xl font-bold mx-auto my-0 font-[Ubuntu,sans-serif] break-words relative text-white p-0 flex-shrink-0 table self-start w-fit box-border"
                  >
                    {{ `0${ 1 + index}` }}
                  </h5>
                </div>
                </div>
              </div>
            </div>
              <p
                class="text-base sm:text-lg my-0 break-words relative p-0 box-border"
              >
                <b class="box-border font-bold"
                  >{{ item.title }}</b
                >
                <br class="box-border" />
                {{ item.description }},&nbsp;<a
                  :href="item.link"
                  target="_blank"
                  class="bg-none p-0 bg-transparent text-[#478ac9] my-0 leading-[28.8px] text-[18px] border-0 border-transparent border-solid inline-block align-baseline whitespace-normal text-left stroke-none no-underline box-border border-t-0 border-l-0 border-r-0 font-['Open_Sans',sans-serif] normal-case transition-[background-color,color,border-color] cursor-pointer font-normal border-0 outline-0 m-0 not-italic select-none rounded-none self-start"
                  >Read More.....</a
                >
              </p>
            </div>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<script setup lang="ts">
interface ProjectItem {
  title: string;
  description: string;
  link?: string;
  linkText?: string;
}

const cadProjects: ProjectItem[] = [
  {
    title:
      "Bridging the Skills Gap in CAD Training for IsDB-BISEW Scholarship Program.",
    description:
      "IsDB-BISEW funds, develops, and carries out projects focused on education, training people, and strengthening organizations in various countries. In Bangladesh,",
    link: "https://scsl.scsl.ltd/scsl/cad-training-for-isdb-bisew",
    linkText: "more info",
  },
  {
    title: "Empowering Madrasah Students with Advanced CAD Skills.",
    description:
      "Our innovative CAD training program provides Madrasah students with industry-ready skills, opening new career pathways and fostering tech inclusion.",
    link: "https://scsl.scsl.ltd/scsl/cad-training-madrasah",
    linkText: "learn more",
  },
  {
    title: "Bangladesh Open University (BOU) CAD Training Collaboration.",
    description:
      "Partnered with BOU to deliver nationwide CAD training, enhancing technical capacity among distance learners through a blended learning model.",
    link: "https://scsl.scsl.ltd/scsl/bou-cad-training",
    linkText: "see details",
  },
];
</script>
