<template>
  <div class="m-4 border-2 border-red-200">
    <Heading msg="Know About Us" />
    <div class="flex flex-col md:flex-row items-center justify-center">
      <img src="/BG/BG-5.webp" class="w-full h-80 rounded m-4 p-1 md:m-2 md:p-0" />
      <div
        class="flex flex-col items-center justify-center m-4 p-1 md:m-2 md:p-0"
      >
        <div class="font-mono text-xl m-auto">
          We are a compassionate team with a focus on building healthy
          communities, strengthening families, and creating opportunities for
          those in hardship! Our project is working towards breaking the cycle
          of poverty to those kids who can't afford education at all. The
          underprivileged community does not have access to quality education
          and our project targets the disadvantaged community. The project aims
          to solve this inequality in education by providing quality education
          to distressed kids .Their families will be benefited from this project
          too
        </div>
        <div>
          <button
            @click="navigateTo('/about')"
            class="w-auto px-4 py-2 m-2 text-red-500 rounded font-mono text-xl border-2 border-red-500 hover:text-white hover:bg-red-500"
          >
            Know more
            <span class="inline-block align-middle"><IconsRightarrow /></span>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>
