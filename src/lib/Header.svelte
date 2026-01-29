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
      <a href="#about" class="hover:text-black transition-colors">About</a>
      <a href="#contact" class="hover:text-black transition-colors">Contact</a>
      <a href="#" class="hover:text-black transition-colors">Schedule Consultation</a>
    </div>
  </div>

  <!-- Main Nav -->
  <div class="border-b border-gray-100">
    <div class="max-w-[1600px] mx-auto px-6 h-20 flex justify-between items-center relative">
      <!-- Logo -->
      <div class="w-48">
        <a href="/" class="block">
          <svg width="88" height="87" viewBox="0 0 88 87" fill="none" xmlns="http://www.w3.org/2000/svg" class="h-10 w-auto">
            <path fill-rule="evenodd" clip-rule="evenodd" d="M19.6908 0C9.01325 0 0.357422 8.65582 0.357422 19.3333V67.6667C0.357422 78.3442 9.01325 87 19.6908 87H68.0241C78.7017 87 87.3574 78.3442 87.3574 67.6667V19.3333C87.3574 8.65582 78.7017 0 68.0241 0H19.6908ZM19.6908 12.0833C15.6867 12.0833 12.4408 15.3292 12.4408 19.3333V67.6667C12.4408 71.6708 15.6867 74.9167 19.6908 74.9167H36.6074C40.6116 74.9167 43.8574 71.6708 43.8574 67.6667V19.3333C43.8574 15.3292 40.6116 12.0833 36.6074 12.0833H19.6908Z" fill="black"/>
          </svg>
        </a>
      </div>

      <!-- Center Nav -->
      <nav class="hidden md:flex items-center gap-10 text-[13px] font-medium tracking-wide uppercase">
        <a href="#models" class="hover:text-gray-600 transition-colors">Design Styles</a>
        <a href="#process" class="hover:text-gray-600 transition-colors">Our Process</a>
        <a href="#why-versa" class="hover:text-gray-600 transition-colors">Why Versa Villa</a>
        <a href="#founders" class="hover:text-gray-600 transition-colors">Our Story</a>
      </nav>

      <!-- Right CTA -->
      <div class="w-48 flex justify-end items-center">
        <a href="#contact" class="bg-black text-white px-6 py-2.5 text-xs uppercase tracking-widest hover:bg-gray-800 transition-colors">
          Get Started
        </a>
      </div>
    </div>
  </div>

  <!-- Sub Nav / Breadcrumb area -->
  <div class="border-b border-gray-100">
    <div class="max-w-[1600px] mx-auto px-6 h-12 flex justify-center items-center">
        <div class="text-[11px] uppercase tracking-wide font-medium text-gray-500">
            <span class="text-primary-600">6-Month Guaranteed Delivery</span> • Fire-Resistant Construction • Fixed Pricing
        </div>
    </div>
  </div>
</header>
