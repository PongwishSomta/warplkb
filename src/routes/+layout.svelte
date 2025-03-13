<script lang="ts">
  import "../app.css";
  let { children } = $props();
  import { ModeWatcher } from "mode-watcher";
  import "@fontsource-variable/noto-sans-thai";
</script>

<ModeWatcher defaultMode="dark" />
<main class="max-w-lg min-h-screen  mx-auto bg-background">
  <div class="flex flex-col items-center justify-center min-h-screen px-4">
    <slot />
  </div>
</main>
