<script>

  const social = [
    {
      name: "Facebook",
      url: "https://www.facebook.com/diyetisyenceren/",
      background: "bg-blue-500",

    },
    {
      name: "Instagram",
      url: "https://www.instagram.com/diyetisyenceren/",
      background: "bg-red-400",

    },
    {
      name: "LinkedIn",
      url: "https://www.linkedin.com/in/berfin-ceren-al%C4%B1%C5%9F%C4%B1r-845b69131/",
      background: "bg-blue-700",

    }
  ];
</script>

<svelte:head>
  <title>Diyetisyen Ceren Alışır - İletişim</title>
</svelte:head>

<section class="max-w-[800px] text-center mx-auto py-10 px-4">
  <div class="text-center mb-10">
    <h1 class="text-2xl text-gray-800">Email ile ulaşın:</h1>
    <a class="text-xl text-blue-700" href="mailto:hello@cerenalisir.com">
      hello@cerenalisir.com
    </a>
  </div>
  <div class="gap-2">
    <h1 class="text-2xl text-gray-800 mb-6">
      Sosyal Ağlardaki Hesaplarım
    </h1>
    <div class="flex flex-wrap gap-4 items-center justify-center">
      {#each social as { name, url, background, icon }}
        <a
          class="block py-2 px-4 w-[10rem] font-semibold text-lg {background} rounded-md text-white flex items-center gap-2"
          href={url}
        >

          {name}
        </a>
      {/each}
    </div>
  </div>
</section>
