<script lang="ts">
  import "../app.css";
  let { children } = $props();
  import { ModeWatcher } from "mode-watcher";
  import "@fontsource-variable/noto-sans-thai";
  import Icon from "@iconify/svelte";
  import Navbar from "$lib/components/ui/navbar.svelte";
  import Footer from "$lib/components/ui/footer.svelte";
</script>

<ModeWatcher defaultMode="dark" />
<main class="max-w-lg min-h-screen mx-auto bg-background">
  <Navbar />
  <div class="flex flex-col items-center justify-center min-h-screen px-4">
    <slot />
  </div>
  <Footer/>
</main>
