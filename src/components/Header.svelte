<script>
  export let y;

  let tabs = [
    { name: "About me", link: "#about" },
    { name: "Portfolio", link: "#portfolio" },
    { name: "Contact", link: "#contact" },
  ];
</script>

<header
  class={"sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border border-none " +
    (y > 0
      ? " py-4 bg-cyan-50  border-emerald-800"
      : " py-6 bg-transparent border-transparent")}
>
  <img src={"images/eadesign.png"} alt="EA Design" class="max-h-[70px]" />

  <div class="sm:flex items-center gap-4 hidden">
    {#each tabs as tab, index}
      <!-- svelte-ignore a11y-missing-attribute -->
      <a
        href={tab.link}
        class="duration-200 hover:text-emerald-800"
        target={index === 2 ? "_blank" : ""}
      >
        <p>{tab.name}</p>
      </a>
    {/each}
  </div>
</header>
