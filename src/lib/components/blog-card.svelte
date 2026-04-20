<script>
    let { title ,date, content,effort, meme } = $props();

    let PostContent = $derived(content);

</script>


<main class="w-screen" >
  <section id="parent"
    class="grid h-screen w-4/5 m-auto mt-1 card preset-filled-surface-100-900 border-[3px] border-surface-200-800  divide-surface-200-800  divide-y overflow-hidden"
  >
    <header class="overflow-hidden ">
      <img src={meme} class="w-full" alt="banner" />
    </header>
    <article class="overflow-y-scroll space-y-4 p-4 span-8">
      <div>
        <h2 class="h6">Självupplevd ansträngning: {effort}</h2>

        <h3 class="h3">{title}</h3>
      </div>
      <p class="opacity-60 ">
          <PostContent />
      </p>
    </article>
    <footer class="flex items-center justify-between gap-4 p-4">
      <small class="opacity-60">Slutprojekt i webbutveckling </small>
      <small class="opacity-60">Publicerat: {date}</small>
    </footer>
  </section>
</main>



<style>

section {
    grid-template-rows: 2fr 7fr 1fr;
    transition: grid-template-rows 300ms ease;
  }

  #parent:has(header:hover) {
    grid-template-rows: 8fr 1fr 1fr;
  }
</style>