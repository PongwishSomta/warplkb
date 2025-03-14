<script lang="ts">
  import Icon from "@iconify/svelte";
  import { cubicOut } from "svelte/easing";
  import { fly } from "svelte/transition";
  import logo from "$lib/images/logo.png";
  import { Button } from "$lib/components/ui/button/index.js";

  let menuOpen = false;

  const toggleMenu = () => {
    menuOpen = !menuOpen;
  };
</script>

<!-- Navbar -->
<nav
  class="fixed top-0 left-0 right-0 z-50 max-w-lg w-full mx-auto backdrop-blur-lg bg-background/80 border-b-border border-b text-white shadow-md"
>
  <div class="flex justify-between items-center p-4">
    <!-- Logo -->
    <a href="/" class="flex items-center gap-2">
      <img src={logo} alt="Logo" class="w-24 h-fit" />
    </a>
    <!-- Hamburger Button -->
    <button
      class="p-2 rounded focus:outline-none"
      on:click={toggleMenu}
      aria-label="Toggle Menu"
    >
      <Icon
        icon={menuOpen ? "carbon:close" : "gg:menu-right"}
        class="w-6 h-6"
      />
    </button>
  </div>

  <!-- Dropdown Menu -->
  {#if menuOpen}
    <div
      transition:fly={{ y: -20, duration: 300, easing: cubicOut }}
      class="flex flex-col items-center  p-4 space-y-2"
    >
      <Button
        class="w-full h-fit bg-primary-foreground text-white text-base py-3 hover:bg-primary-foreground hover:ring-[1px] hover:ring-gray-800 "
        href="/login"
      >
        <p>เข้าสู่ระบบ</p>
      </Button>
      <Button
        class="w-full h-fit bg-primary-foreground text-white text-base py-3 hover:bg-primary-foreground hover:ring-[1px] hover:ring-gray-800 "
        href="/register"
      >
        <p>สมัครสมาชิก</p>
      </Button>
    </div>
  {/if}
</nav>
