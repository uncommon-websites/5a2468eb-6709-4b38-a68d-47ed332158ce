<script lang="ts">
  import { onMount } from 'svelte';

  let isScrolled = false;

  onMount(() => {
    const handleScroll = () => {
      isScrolled = window.scrollY > 50;
    };
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  });
</script>

<header class="w-full bg-white text-gray-900 sticky top-0 z-50 transition-all duration-300">
  <!-- Top Bar -->
  <div class="border-b border-gray-100 hidden md:block">
    <div class="max-w-[1600px] mx-auto px-6 h-10 flex justify-end items-center gap-6 text-[11px] font-medium tracking-wide text-gray-500 uppercase">
      <a href="#" class="hover:text-black transition-colors">News</a>
      <a href="#" class="hover:text-black transition-colors">Pro</a>
      <a href="#" class="hover:text-black transition-colors">Contact</a>
      <button class="hover:text-black transition-colors flex items-center gap-1">En <span class="text-[8px]">▼</span></button>
      <button class="hover:text-black transition-colors flex items-center gap-1">Gbp <span class="text-[8px]">▼</span></button>
    </div>
  </div>

  <!-- Main Nav -->
  <div class="border-b border-gray-100">
    <div class="max-w-[1600px] mx-auto px-6 h-20 flex justify-between items-center relative">
      <!-- Logo -->
      <div class="w-32">
        <a href="/" class="text-2xl font-bold tracking-tight font-display text-orange-400">
          <!-- SVG Logo Placeholder -->
           <span class="text-black">Dinesen</span>
        </a>
      </div>

      <!-- Center Nav -->
      <nav class="hidden md:flex items-center gap-10 text-[13px] font-medium tracking-wide uppercase">
        <a href="#" class="hover:text-gray-600 transition-colors">Floors</a>
        <a href="#" class="hover:text-gray-600 transition-colors">Floor Planner</a>
        <a href="#" class="hover:text-gray-600 transition-colors">Inspiration</a>
        <a href="#" class="hover:text-gray-600 transition-colors">Shop</a>
      </nav>

      <!-- Right Icons -->
      <div class="w-32 flex justify-end items-center gap-6">
        <button aria-label="Search" class="hover:text-gray-600">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5">
            <path stroke-linecap="round" stroke-linejoin="round" d="m21 21-5.197-5.197m0 0A7.5 7.5 0 1 0 5.196 5.196a7.5 7.5 0 0 0 10.607 10.607Z" />
          </svg>
        </button>
        <button aria-label="Cart" class="hover:text-gray-600 relative">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5">
            <path stroke-linecap="round" stroke-linejoin="round" d="M15.75 10.5V6a3.75 3.75 0 1 0-7.5 0v4.5m11.356-1.993 1.263 12c.07.665-.45 1.243-1.119 1.243H4.25a1.125 1.125 0 0 1-1.12-1.243l1.264-12A1.125 1.125 0 0 1 5.513 7.5h12.974c.576 0 1.059.435 1.119 1.007ZM8.625 10.5a.375.375 0 1 1-.75 0 .375.375 0 0 1 .75 0Zm7.5 0a.375.375 0 1 1-.75 0 .375.375 0 0 1 .75 0Z" />
          </svg>
          <span class="absolute -top-1 -right-1 bg-gray-900 text-white text-[9px] w-3.5 h-3.5 flex items-center justify-center rounded-full">0</span>
        </button>
      </div>
    </div>
  </div>

  <!-- Sub Nav / Breadcrumb area -->
  <div class="border-b border-gray-100">
    <div class="max-w-[1600px] mx-auto px-6 h-12 flex justify-end items-center">
        <button class="text-[11px] uppercase tracking-wide font-medium text-gray-500 flex items-center gap-2 hover:text-black">
            More inspiration
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-3 h-3">
                <path stroke-linecap="round" stroke-linejoin="round" d="m19.5 8.25-7.5 7.5-7.5-7.5" />
            </svg>
        </button>
    </div>
  </div>
</header>
