<script>
  export let y;
  let burger = 1;
  function clickBurger() {
    let list = document.querySelector("ul");
    burger === 1
      ? ((burger = 2),
        list.classList.add("top-[80px]"),
        list.classList.add("opacity-100"),
        list.classList.add("bg-white"),
        list.classList.add("text-right"))
      : ((burger = 1),
        list.classList.remove("top-[80px]"),
        list.classList.remove("opacity-100"),
        list.classList.remove("bg-white"),
        list.classList.remove("text-right"));
  }
</script>

<header
  class={"sticky z-[10] top-0 duration-200 px-6 flex items-center justify-between border border-none " +
    (y > 0
      ? " py-4 bg-cyan-50  border-emerald-800"
      : " py-6 bg-transparent border-transparent")}
>
  <img src={"images/eadesign.png"} alt="EA Design" class="max-h-[70px]" />

  <span class="text-3xl cursor-pointer mx-2 md:hidden block">
    <button name="menu" on:click={clickBurger}>&#9776;</button>
  </span>

  <ul
    class="md:bg-cyan-50 md:flex md:items-center z-[-1] md:z-auto md:static absolute w-full left-0 md:w-auto md:py-0 py-4 md:pl-0 pl-7 md:opacity-100 opacity-0 top-[-400px]"
  >
    <li class="mx-4 my-6 md:my-0">
      <a href="#about" class="duration-200 hover:text-emerald-800">About me</a>
    </li>
    <li class="mx-4 my-6 md:my-0">
      <a href="#portfolio" class="duration-200 hover:text-emerald-800"
        >Portfolio</a
      >
    </li>
    <li class="mx-4 my-6 md:my-0">
      <a href="#contact" class="duration-200 hover:text-emerald-800"
        >Contact me</a
      >
    </li>
  </ul>
</header>
