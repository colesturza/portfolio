<script lang="ts">
  import { page } from '$app/stores';
  let mobileMenuClosed = true;
</script>

<!-- nav -->
<nav class="bg-slate-100 shadow-md">
  <div class="max-w-7xl mx-auto px-8">
    <div class="flex justify-between">
      <!-- primary nav -->
      <div class="flex items-center space-x-1">
        {#if $page.url.pathname !== '/'}
          <a href="/" class="py-3 px-3">
            <!-- prettier-ignore -->
            <h1 class="font-extrabold text-transparent text-2xl bg-clip-text bg-gradient-to-r from-purple-500 to-pink-600">
              Cole Sturza
            </h1>
          </a>
        {/if}
      </div>

      <!-- secondary nav -->
      <!-- prettier-ignore -->
      <div class="hidden md:flex items-center space-x-1">
        <a href="/" class="py-4 px-3 text-gray-700 hover:text-purple-700 {$page.url.pathname === '/' ? 'text-purple-700' : ''}">About</a>
        <a href="/resume" class="py-4 px-3 text-gray-700 hover:text-purple-700 {$page.url.pathname === '/resume' ? 'text-purple-700' : ''}">R&eacute;sum&eacute;</a>
        <a href="/cv" class="py-4 px-3 text-gray-700 hover:text-purple-700 {$page.url.pathname === '/cv' ? 'text-purple-700' : ''}">Curriculum Vitae</a>
        <a href="/projects" class="py-4 px-3 text-gray-700 hover:text-purple-700 {$page.url.pathname === '/projects' ? 'text-purple-700' : ''}">Projects</a>
        <a href="/blog" class="py-4 px-3 text-gray-700 hover:text-purple-700 {$page.url.pathname === '/blog' ? 'text-purple-700' : ''}">Blog</a>
      </div>

      <div class="md:hidden flex items-center">
        <button class="py-4 px-3" on:click={() => (mobileMenuClosed = !mobileMenuClosed)}>
          {#if mobileMenuClosed}
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              class="w-6 h-6"
            >
              <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
            </svg>
          {:else}
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 24 24"
              stroke-width="1.5"
              stroke="currentColor"
              class="w-6 h-6"
            >
              <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
            </svg>
          {/if}
        </button>
      </div>
    </div>
  </div>

  <!-- mobile menu -->
  <!-- prettier-ignore -->
  <div class="{mobileMenuClosed ? 'hidden' : ''} md:hidden">
    <a href="/" class="block py-2 px-4 text-sm hover:text-purple-700 {$page.url.pathname === '/about' ? 'text-purple-700' : ''}">About</a>
    <a href="/resume" class="block py-2 px-4 text-sm hover:text-purple-700 {$page.url.pathname === '/resume' ? 'text-purple-700' : ''}">R&eacute;sum&eacute;</a>
    <a href="/cv" class="block py-2 px-4 text-sm hover:text-purple-700 {$page.url.pathname === '/cv' ? 'text-purple-700' : ''}">Curriculum Vitae</a>
    <a href="/projects" class="block py-2 px-4 text-sm hover:text-purple-700 {$page.url.pathname === '/projects' ? 'text-purple-700' : ''}">Projects</a>
    <a href="/blog" class="block py-2 px-4 text-sm hover:text-purple-700 {$page.url.pathname === '/blog' ? 'text-purple-700' : ''}">Blog</a>
  </div>
</nav>
