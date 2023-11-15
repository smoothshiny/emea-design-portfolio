<script>
  import Step from "./Step.svelte";

  let steps = [

    { name: "Ohio University", icon: "fa-solid fa-school" }
  ];

  let benefits = [
    {
      metric: "10x",
      name: "Artist Statement",
      description:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla sed nisl sed libero malesuada feugiat et eu neque. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Sed nunc tortor, pretium vel ultricies nec, mattis sit amet quam. Nullam tempus rhoncus tellus, quis cursus magna rhoncus at.",
    },
  ];
</script>

<main class="flex flex-col flex-1 p-4">
  <section
    id="intro"
    class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
  >
    <div
      class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
    >
      <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
        Welcome to EA design!
      </h2>
      <p class="text-base sm:text-lg md:text-xl">
        My goal as a graphic designer is to create visually appealing products
        and build professional connections with my clients.
      </p>
      <img
        src={"images/Ella.png"}
        alt="Ella Atfield"
        class="object-cover z-[2] max-h-[70vh]"
      />
      <button
        class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-emerald-800 text-cyan-50"
      >
        <div
          class="absolute top-0 right-full w-full h-full bg-orange-500 opacity-90 group-hover:translate-x-full z-0 duration-200"
        />
        <h4 class="relative z-9">Contact me &rarr;</h4>
      </button>
    </div>
    <div class="relative shadow-2xl grid place-items-center" />
  </section>
  <section
    id="about"
    class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
  >
    <div
      class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-emerald-800 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-emerald-800 py-4"
    >
      <h6 class="text-large sm:text-xl md:text-2xl">Want to know more?</h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        A bit <span class="poppins text-emerald-800">about</span> me.
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
    <a
      href="https://youtu.be/CVxddtLF8Zg?si=FH-dE9TvBsoSBKxI"
      target="_blank"
      class="mx-auto px-4 py-2 rounded-md border border-solid border-black flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-green-700 duration-200"
    >
      <i class="fa-regular fa-circle-play" />
      <p>Watch the Video!</p>
    </a>
    <br /><br />
    <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
      <Step step={steps[0]} />
    </div>
  </section>
</main>
