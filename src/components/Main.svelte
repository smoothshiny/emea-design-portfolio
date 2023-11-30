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

  let openTab = 1;

  function toggleTabs(tabNumber) {
    openTab = tabNumber;
  }
</script>

<main class="flex flex-col flex-1 p-4">
  <section id="intro" class="grid grid-cols-1 sm:py-14">
    <div
      class="flex flex-col place-items-center lg:text-left m-20 gap-6 md:gap-8 lg:gap-10"
    >
      <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
        Welcome to EA design!
      </h2>

      <button
        class="blueShadow place-items-center lg:text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-emerald-800 text-cyan-50"
        ><h4 class="relative z-9">Contact me &rarr;</h4>
      </button>
    </div>
  </section>

  <section
    id="about"
    class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
  >
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
            <h3 class="text-center text-2xl sm:text-3xl md:text-5xl">
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
    <div class="flex flex-wrap">
      <div class="w-full">
        <ul class="flex mb-0 list-none flex-wrap pt-3 pb-4 flex-row">
          <li class="-mb-px mr-2 last:mr-0 flex-auto text-center">
            <a
              class="text-xs font-bold uppercase px-5 py-3 shadow-lg rounded block leading-normal {openTab ===
              1
                ? 'text-white bg-emerald-800'
                : 'text-orange-600 bg-white'}"
              on:click={() => toggleTabs(1)}
            >
              OU Printing Services
            </a>
          </li>
          <li class="-mb-px mr-2 last:mr-0 flex-auto text-center">
            <a
              class="text-xs font-bold uppercase px-5 py-3 shadow-lg rounded block leading-normal {openTab ===
              2
                ? 'text-white bg-emerald-800'
                : 'text-orange-600 bg-white'}"
              on:click={() => toggleTabs(2)}
            >
              Class Projects
            </a>
          </li>
          <li class="-mb-px mr-2 last:mr-0 flex-auto text-center">
            <a
              class="text-xs font-bold uppercase px-5 py-3 shadow-lg rounded block leading-normal {openTab ===
              3
                ? 'text-white bg-emerald-800'
                : 'text-orange-600 bg-white'}"
              on:click={() => toggleTabs(3)}
            >
              Commissions
            </a>
          </li>
        </ul>
        <div
          class="relative flex flex-col min-w-0 break-words bg-white w-full mb-6 shadow-lg rounded"
        >
          <div class="px-4 py-5 flex-auto">
            <div class="tab-content tab-space">
              <div class={openTab === 1 ? "block" : "hidden"}>
                <p>
                  In hac habitasse platea dictumst. Pellentesque habitant morbi
                  tristique senectus et netus et malesuada fames ac turpis
                  egestas. Suspendisse potenti. Suspendisse id bibendum turpis,
                  sit amet vehicula mi. Quisque fringilla hendrerit scelerisque.
                  <br />
                  <br />
                  Proin efficitur dui in pulvinar semper. Vestibulum suscipit at
                  leo in venenatis. Ut sollicitudin turpis a lectus sagittis vestibulum.
                  Suspendisse vehicula porta ligula in ornare. Curabitur dictum elit
                  a sapien placerat, non aliquam mi interdum. Suspendisse varius
                  massa quis lacus vehicula faucibus.
                </p>
              </div>
              <div class={openTab === 2 ? "block" : "hidden"}>
                <p>
                  Morbi consectetur mauris non nunc dapibus, in cursus tortor
                  ornare. Sed vel porttitor felis, at cursus nulla. Integer
                  facilisis sed massa at porta. Nulla consectetur ligula
                  interdum, semper dolor nec, maximus tortor. Nam nec libero
                  gravida enim tincidunt ultricies. Vestibulum nec mi dapibus,
                  lacinia sapien sed, fermentum magna.
                  <br />
                  <br />
                  Ut dictum diam dui, eu fermentum quam ullamcorper imperdiet. Aliquam
                  commodo nulla sed lorem blandit, non vestibulum mauris faucibus.
                  Ut tincidunt enim velit, sagittis condimentum dui vestibulum vitae.
                </p>
              </div>
              <div class={openTab === 3 ? "block" : "hidden"}>
                <p>
                  Pellentesque congue iaculis nunc, vitae ultrices arcu placerat
                  eu. Fusce quis ipsum non felis facilisis porttitor. Sed
                  volutpat dignissim magna, ornare lobortis ex laoreet ac.
                  Nullam blandit dolor nec ullamcorper tristique. Nulla pretium
                  arcu ac nibh finibus consectetur. Fusce vitae ultricies sem.
                  Maecenas sit amet facilisis risus. Nulla varius lectus in
                  lorem placerat viverra.
                  <br />
                  <br />
                  Nullam leo nibh, vulputate sodales euismod a, egestas quis dolor.
                  Duis porttitor nec neque vel ornare. Nunc id ornare nulla. Nam
                  sit amet nulla nibh.
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</main>
