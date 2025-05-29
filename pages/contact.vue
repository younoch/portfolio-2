<template>
  <section class="">
    <div class="relative w-full h-[180px] sm:h-[250px] overflow-hidden">
      <!-- Background Video -->
      <video
        autoplay
        loop
        muted
        playsinline
        class="absolute top-0 left-0 w-full h-full object-cover z-0"
      >
        <source
          src="https://scsl.scsl.ltd/global/files/scsl_banner_vid.mp4"
          type="video/mp4"
        />
        Your browser does not support the video tag.
      </video>

      <!-- Overlay (optional for better text visibility) -->
      <div class="absolute inset-0 bg-black/40 z-10"></div>

      <!-- Foreground Content -->
      <div
        class="relative z-20 flex flex-col justify-center items-center h-full text-white px-4"
      >
        <h1 class="font-bold text-3xl sm:text-5xl font-roboto text-center mb-2">
          Contact Us
        </h1>
        <p class="text-sm md:text-base text-center text-gray-200">
          How Can We Help?
        </p>
      </div>
    </div>

    <div
      class="max-w-6xl mx-auto pt-3 sm:pt-6 w-full grid grid-cols-12 gap-2 md:gap-4"
    >
      <div
        class="col-span-6 md:col-span-3 bg-cyan-700 text-white flex flex-col md:flex-row justify-between items-center rounded-lg ga-2 md:gap-4 p-2 md:p-4"
      >
        <UIcon name="i-mdi-phone" size="32" />
        <div class="flex flex-col flex-1">
          <p class="font-semibold md:text-lg">Phone Number</p>
          <div class="flex-1 text-center md:text-left">
            <p class="flex-1 text-sm md:text-base text-center md:text-left">+91 80004 36640</p>
          </div>
        </div>
      </div>
      <div
        class="col-span-6 md:col-span-3 bg-cyan-700 text-white flex flex-col md:flex-row justify-between items-center rounded-lg gap-1 md:gap-4 p-2 md:p-4"
      >
        <UIcon name="i-mdi-email" size="32" />
        <div class="flex flex-col flex-1">
          <p class="font-semibold md:text-lg text-center md:text-left">Email</p>
          <p class="flex-1 text-sm md:text-base text-center md:text-left">info@stargroup-bd.com</p>
        </div>
      </div>
      <div
        class="col-span-6 md:col-span-3 bg-cyan-700 text-white flex flex-col md:flex-row justify-between items-center rounded-lg ga-2 md:gap-4 p-2 md:p-4"
      >
        <UIcon name="i-mdi-map-marker" size="32" />
        <div class="flex flex-col flex-1">
          <p class="font-semibold md:text-lg text-center md:text-left">Location</p>
          <p class="flex-1 text-sm md:text-base text-center md:text-left">
            Fattah Plaza(7th floor) 70 Green Road Dhaka 1205, Bangladesh
          </p>
        </div>
      </div>
      <div
        class="col-span-6 md:col-span-3 bg-cyan-700 text-white flex flex-col md:flex-row justify-between items-center rounded-lg gap-4 p-4"
      >
        <UIcon name="i-mdi-clock-outline" size="32" />
        <div class="flex flex-col flex-1">
          <p class="font-semibold md:text-lg text-center md:text-left">Working Hours</p>
          <p class="flex-1 text-sm md:text-base text-center md:text-left">Monday to Saturday <br />09:00 AM to 06:00 PM</p>
        </div>
      </div>

      <div
        class="pt-6 relative min-h-[1px] px-4 box-border rounded-3xl col-span-12 md:col-span-7"
      >
        <UForm
          class="grid grid-cols-2 gap-2 md:gap-4"
          :validate="false"
          @submit="submitForm"
        >
          <!-- Full Name -->
          <div class="col-span-2">
            <UFormGroup
              label="Full Name:"
              name="name"
              :ui="{ label: 'text-teal-600 font-medium' }"
            >
              <UInput
                v-model="form.name"
                placeholder="Enter Full Name"
                required
                :ui="{
                  base: 'border-teal-500 focus:ring-teal-500 focus:border-teal-500',
                }"
              />
            </UFormGroup>
          </div>

          <!-- Email -->
          <div>
            <UFormGroup
              label="Email Address:"
              name="email"
              :ui="{ label: 'text-teal-600 font-medium' }"
            >
              <UInput
                v-model="form.email"
                type="email"
                placeholder="Enter Email"
                required
                :ui="{
                  base: 'border-teal-500 focus:ring-teal-500 focus:border-teal-500',
                }"
              />
            </UFormGroup>
          </div>

          <!-- Phone -->
          <div>
            <UFormGroup
              label="Phone Number:"
              name="phone"
              :ui="{ label: 'text-teal-600 font-medium' }"
            >
              <UInput
                v-model="form.phone"
                type="tel"
                placeholder="Enter Phone Number"
                required
                :ui="{
                  base: 'border-teal-500 focus:ring-teal-500 focus:border-teal-500',
                }"
              />
            </UFormGroup>
          </div>

          <!-- Service Type -->
          <div>
            <UFormGroup
              label="Service Type:"
              name="service"
              :ui="{ label: 'text-teal-600 font-medium' }"
            >
              <USelect
                v-model="form.service"
                :options="serviceOptions"
                placeholder="Select a Service"
                required
                :ui="{
                  base: 'border-teal-500 focus:ring-teal-500 focus:border-teal-500',
                }"
              />
            </UFormGroup>
          </div>

          <!-- File Upload -->
          <div>
            <UFormGroup
              label="Attachment (optional):"
              name="attachment"
              :ui="{ label: 'text-teal-600 font-medium' }"
            >
              <UInput
                type="file"
                @change="handleFile"
                :ui="{
                  base: 'border-teal-500 focus:ring-teal-500 focus:border-teal-500',
                }"
              />
            </UFormGroup>
          </div>

          <!-- Message -->
          <div class="col-span-2">
            <UFormGroup
              label="Message:"
              name="message"
              :ui="{ label: 'text-teal-600 font-medium' }"
            >
              <UTextarea
                v-model="form.message"
                placeholder="Enter your message"
                rows="4"
                :ui="{
                  base: 'border-teal-500 focus:ring-teal-500 focus:border-teal-500',
                }"
              />
            </UFormGroup>
          </div>

          <!-- Submit Button -->
          <div class="col-span-2 flex justify-center md:justify-end">
            <UButton type="submit" color="teal"> Submit Request </UButton>
          </div>
        </UForm>
      </div>

      <div class="col-span-12 md:col-span-5">
        <img
          src="/public/images/WhatsAppImage2025-05-15at14.49.33_641779d9.jpg"
          width="100%"
          height="auto"
        />
      </div>
    </div>
  </section>
</template>
<script setup>
const form = ref({
  name: "",
  email: "",
  phone: "",
  service: "",
  attachment: null,
  message: "",
});

const serviceOptions = [
  { label: "Installation", value: "installation" },
  { label: "Maintenance", value: "maintenance" },
  { label: "Repair", value: "repair" },
];

function handleFile(event) {
  form.value.attachment = event.target.files[0];
}

function submitForm() {
  // Here you can send `form.value` to an API or handle it however needed
  console.log("Submitted Form:", form.value);
}
</script>
