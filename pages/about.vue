<template>
  <div class="m-2">
    <Heading msg="Know about us!" />
    <div class="flex flex-col">
      <div class="flex flex-col md:flex-row items-center justify-center m-5">
        <div
          class="md:w-1/2 text-center font-serif text-3xl mb-4 font-extrabold"
        >
          {{ "Transform Lives: Join Us in Making a Difference!" }}
        </div>
        <div class="md:w-1/2 text-left">
          <p class="font-semibold font-serif text-xl mb-2">
            {{ "We help underprivileged sections of society to uplift" }}
          </p>
          <p class="font-mono text-xl">
            {{
              "We work for the development of the Bastis in the Kanpur region of UP, helping in education, health and finance. We continuously organizes events and awareness sessions in those areas, making them aware of government schemes, scholarships and health. We aims to uplift those underprivileged sections of society."
            }}
          </p>
        </div>
      </div>
      <div class="flex flex-col items-center m-5">
        <iframe
          src="https://www.youtube.com/embed/E4_sd7NiFLI?si=60mes1-KzUY5AlA-"
          title="आशा की किरण कहानी"
          class="w-full md:w-9/12 h-96"
        ></iframe>
      </div>
      <div class="flex flex-col md:flex-row items-center md:items-start m-5">
        <div class="md:w-1/2 text-left my-2 md:m-2">
          <Heading msg="Our Mission" class="my-2" />
          <p class="font-semibold font-serif text-xl mb-2">
            {{ "We make the society we save our own humanity" }}
          </p>
          <p class="font-mono text-xl">
            {{
              "Works for the development of the bastis in the Kanpur region of UP, helping in education, health and finance. We continuously organizes events and awareness sessions in those areas, making them aware of government schemes, scholarships and health. This organization aims to uplift those underprivileged sections of society."
            }}
          </p>
        </div>
        <div class="md:w-1/2 text-left my-2 md:m-2">
          <Heading msg="Our Vision" class="my-2" />
          <p class="font-semibold font-serif text-xl mb-2">
            {{ "Better today, brighter tomorrow" }}
          </p>
          <p class="font-mono text-xl">
            {{
              "We seek a world of hope, tolerance and social justice, where poverty has been overcome and people live in dignity and security. The villages must be potential enough to develop at a faster pace, the  underprivileged sections of society must rise.  "
            }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>
