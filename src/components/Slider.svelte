<script>
  export let duration;
  export let slides;
  let currentSlide = 0;

  const nextSlide = () => {
    currentSlide++;
    if (currentSlide >= slides.length) {
      currentSlide = 0;
    }
    timer();
  };

  const previousSlide = () => {
    currentSlide++;
    if (currentSlide <= slides.length - 1) {
      currentSlide = 0;
    }
    timer();
  };
  const goToSlide = (i) => {
    currentSlide = i;
    timer();
  };
  let interval;
  const timer = () => {
    clearInterval(interval);
    interval = setInterval(nextSlide, duration);
  };
  timer();
</script>

<div class="slider">
  {#each slides as slider, i}
    {#if currentSlide === i}
      <div class="slide" transition:blur={{ amount: 10 }}>
        <img src={slider} />
      </div>
    {/if}
  {/each}
  <button class="next" on:click={nextSlide}>next</button>
  <button class="prev absolute" on:click={previousSlide}>previous</button>
  <div class="nav">
    {#each slides as slider, i}
      <button
        class="bubble"
        on:click={() => {
          goToSlide(i);
        }}>^</button
      >
    {/each}
  </div>
</div>

<style>
  .slider {
    width: 100vw;
    height: 100vh;
    position: relative;
  }
  .slide {
    position: absolute;
    inset: 0;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .nav {
    position: absolute;
    bottom: 20px;
    left: 0;
    right: 0;
    height: 50px;
    z-index: 3;
    display: flex;
  }
  .bubble {
    padding: 0;
    border: 0;
    height: 20px;
    width: 20px;
    border-radius: 100px;
    transition: all 0.3s ease-out;
    cursor: pointer;
  }
</style>
