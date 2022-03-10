<script>

  import { page } from "$app/stores";

  const menu = [
    { name: "Merhaba", url: "/",  },
    { name: "İletişim", url: "/iletisim", },
 //   { name: "Instagram", url: "/instagram", icon: GalleryIcon },
    { name: "Blog", url: "/blog", }
   
  ];
</script>

<header
  class="bg-white w-100 py-10 flex items-center justify-center border-b-2"
>
  <div class="text-center max-w-[960px] px-4 flex flex-col">
    <img
      class="rounded-full mx-auto w-[10rem] h-[10rem] shadow-md"
      alt="Diyetisyen Ceren Alışır"
      src="/diyetisyen-ceren-alisir.jpg"
    />
    <span class="block text-4xl mt-6 font-bold text-gray-900">
      Diyetisyen CEREN ALIŞIR
    </span>
    <p class="text-xl leading-8 text-gray-800 font-bold mt-2">
      Kanıta Dayalı Sağlıklı Sürdürülebilir Beslenme Danışmanlığı
    </p>
    <p class="text-lg leading-8 text-gray-600 font-bold mb-2">
      #diyet #onlinediyet #hastalıklardadiyet #insülindirenci <br/>#diyabettebeslenme #sagliklibeslenme #sezgiselyeme #yemefarkındalığı
    </p>
    <div class="flex">
      <a
      href="https://www.linkedin.com/in/berfin-ceren-al%C4%B1%C5%9F%C4%B1r-845b69131/"
      class="mt-4 mr-2 px-4 py-2 rounded-md bg-blue-600 hover:bg-blue-500 transition-colors text-white font-bold text-md flex items-center justify-center gap-2 mx-auto"
    >
    
      LinkedIn'de Takip Et
    </a>
    <a
      href="https://www.instagram.com/diyetisyenceren/"
      class="mt-4 ml-2 px-4 py-2 rounded-md bg-blue-600 hover:bg-blue-500 transition-colors text-white font-bold text-md flex items-center justify-center gap-2 mx-auto"
    >
    
      Instagram'da Takip Et
    </a>
    </div>
    
  </div>
</header>

<nav class="mx-auto max-w-[960px] py-2 px-4 flex items-center justify-center">
  {#each menu as { name, url, icon }}
    <div
      class={`relative px-4 py-2 mt-[-10px] flex items-center justify-center gap-2 ${
        $page.url.pathname === url
          ? "menu rounded-bl-md rounded-br-md border-b-2 border-l-2 border-r-2 border-gray-200 bg-white text-gray-900"
          : "text-gray-600"
      }`}
    >
      <svelte:component this={icon} class="w-4 h-4" />
      <a class="text-lg" href={url}>{name}</a>
    </div>
  {/each}
</nav>

<style>
  header{
    background-image: url("/pexels-ella-olsson-1640770.jpg");
    @apply bg-bottom bg-cover;
  }
  .menu::before {
    content: "";
    position: absolute;
    left: 0;
    right: 0;
    top: -1rem;
    background-color: white;
    height: 1rem;
  }
</style>
