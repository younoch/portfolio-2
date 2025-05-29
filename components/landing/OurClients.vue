<template>
  <section class="py-12 px-4 sm:px-6 lg:px-8 bg-white">
    <div class="max-w-7xl mx-auto">
      <h2 class="text-3xl sm:text-4xl md:text-5xl font-bold text-center text-gray-900 mb-12">
        Some Of Our Clients
      </h2>
      
      <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-6 xl:grid-cols-8 gap-6">
        <div 
          v-for="(client, index) in clients" 
          :key="index"
          class="flex items-center justify-center p-4 bg-white rounded-lg shadow-sm hover:shadow-md transition-shadow duration-300"
        >
          <img 
            :alt="'Client logo ' + (index + 1)" 
            :src="'/images/' + client.image" 
            class="w-full h-16 object-contain"
            loading="lazy"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const clients = [
  { image: "Untitleddesign12.png" },
  { image: "Untitleddesign13.png" },
  { image: "Untitleddesign11.png" },
  { image: "Untitleddesign6.png" },
  { image: "Untitleddesign4.png" },
  { image: "Untitleddesign5.png" },
  { image: "Untitleddesign7.png" },
  { image: "Untitleddesign10.png" },
  { image: "Untitleddesign21.png" },
  { image: "Untitleddesign1.png" },
  { image: "Untitleddesign20.png" },
  { image: "Untitleddesign9.png" },
  { image: "Untitleddesign8.png" },
  { image: "Untitleddesign19.png" },
  { image: "Untitleddesign3.png" },
  { image: "Untitleddesign18.png" },
  { image: "Untitleddesign17.png" },
  { image: "Untitleddesign25.png" },
  { image: "Untitleddesign16.png" },
  { image: "Untitleddesign2.png" },
  { image: "Untitleddesign14.png" },
  { image: "Untitleddesign22.png" },
  { image: "Untitleddesign15.png" },
  { image: "Untitleddesign24.png" }
]
</script>