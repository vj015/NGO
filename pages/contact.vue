<template>
  <div class="m-2">
    <Heading msg="Contact us!" />
    <div class="flex md:flex-row flex-col items-center justify-center">
      <div class="md:w-1/2 text-center font-serif text-3xl m-4">
        <p class="mb-2 font-extrabold">{{ "We'd love to hear from you" }}</p>
        <p class="text-xl font-normal text-center">
          {{
            "Have any question in mind or want to enquire? Please feel free to contact us through the form or the following details."
          }}
        </p>
      </div>
      <div
        class="md:w-1/2 text-center font-mono text-xl flex flex-col items-center"
      >
        <div class="m-2">
          <p class="text-2xl font-semibold">{{ "Let's talk! " }}</p>
          <p>{{ "+91-90765226926, +91-8601170114" }}</p>
        </div>
        <div class="m-2">
          <p class="text-2xl font-semibold">{{ "Headoffice" }}</p>
          <p>{{ "114 Krishna lane, Arya Nagar, Varanasi-231133" }}</p>
        </div>
        <div class="m-2">
          <sociallinks />
        </div>
      </div>
    </div>
  </div>
</template>
