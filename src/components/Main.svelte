<script>
  import Step from "./Step.svelte";

  let steps = [{ name: "Ohio University", icon: "fa-solid fa-school" }];

  let benefits = [
    {
      metric: "10x",
      name: "Artist Statement",
      description:
        "My name is Ella Atfied and I am a Graphic Designer based in Cleveland, Ohio. I specialize in all types of design such as logo, brand and package design, as well as t-shirt graphics and poster design and I am a few months away from earning my BFA in Graphic Design from Ohio University. Outside of design, I enjoy grounding activities such as traveling, exploring the outdoors and cooking. I try hard to infuse the positivity from this lifestyle into my design work. My goal for my professional future is to focus on crafting visually appealing products and building connections with clients. Explore the rest of my website to learn more about me and my work!",
    },
  ];
</script>

<main class="flex flex-col flex-1 p-4">
  <section
    id="intro"
    class="grid grid-cols-1 sm:py-14"
  >
    <div
      class="flex flex-col lg:text-left m-20 gap-6 md:gap-8 lg:gap-10"
    >
      <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
        Welcome to EA design!
      </h2>
      <p class="text-base sm:text-lg md:text-xl">
        My goal as a graphic designer is to create visually appealing products
        and build professional connections with my clients.
      </p>

      <button
        class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-emerald-800 text-cyan-50"
      ><h4 class="relative z-9">Contact me &rarr;</h4>
      </button>
    </div>
    <div class="relative shadow-2xl grid place-items-center" />
  </section>
  
  
  
  <section
    id="about"
    class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
    <div
      class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-emerald-800 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-emerald-800 py-4"
    >
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
      <span class="poppins text-emerald-800">About</span> me
      </h3>
    </div>

    <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
      {#each benefits as benefit, index}
        <div class="flex gap-6 sm:gap-8">
          <p
            class="poppins text-4xl sm:text-5xl md:text-6xl text-cyan-50 font-semibold"
          />
          <div class="flex flex-col gap-6 sm:gap-8">
            <h3 class="text-2xl sm:text-3xl md:text-5xl">
              {benefit.name}
            </h3>
            <p>{benefit.description}</p>
          </div>
        </div>
      {/each}
    </div>

  </section>

  <!--Portfolio Section-->
  <section id="portfolio" class="py-20 lg:py-32 flex flex-col gab-24">
    <div class="flex flex-col gap-2 text-center">
      <h6 class="text-lg sm:text-xl md:text-2xl">A few of my projects!</h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        Curious to see my work?
      </h3>
    </div>
    <br /><br /><br />
  </section>
</main>
