<script lang="ts">
  import { Button } from "$lib/components/ui/button/index.js";
  import { Input } from "$lib/components/ui/input/index.js";
  import { Label } from "$lib/components/ui/label/index.js";
  import { Toaster } from "$lib/components/ui/sonner/index.js";
  import Icon from "@iconify/svelte";
  import logo from "$lib/images/logo.png";
  import { goto } from "$app/navigation";

  let username = "";
  let password = "";
  let isLoading = false;
  let showPassword = false;

  async function handleLogin() {
    if (!username || !password) {
      Toaster("error", {
        title: "กรุณากรอกข้อมูลให้ครบถ้วน",
      });
      return;
    }

    isLoading = true;

    try {
      // Replace with your actual authentication logic
      await new Promise((resolve) => setTimeout(resolve, 1000));

      // Simulate successful login (replace with actual API call)
      if (username === "admin" && password === "password") {
        Toaster("success", {
          title: "เข้าสู่ระบบสำเร็จ",
        });

        // Store auth token/session
        localStorage.setItem("adminAuth", "true");

        // Redirect to admin dashboard
        goto("/admin/dashboard");
      } else {
        Toaster("error", {
          title: "เข้าสู่ระบบไม่สำเร็จ",
        });
      }
    } catch (error) {
      Toaster("error", {
        title: "เกิดข้อผิดพลาด",
      });
    } finally {
      isLoading = false;
    }
  }
</script>

<div
  class="flex min-h-screen w-full flex-col items-center justify-center bg-background "
>
  <div class="w-full space-y-6 rounded-xl bg-background p-6 shadow-lg">
    <div class="flex flex-col items-center gap-2">
      <img src={logo} alt="WarpLKB" class="h-20 w-fit" />
      <h1 class="text-2xl font-semibold text-white">ระบบจัดการร้าน</h1>
      <p class="text-sm text-zinc-400">กรุณาเข้าสู่ระบบเพื่อดำเนินการต่อ</p>
    </div>

    <div class="space-y-4">
      <div class="space-y-2">
        <div class="relative">
          <p
            class="absolute left-3 top-2 text-xs leading-4 font-medium opacity-50"
          >
            อีเมล | Email
          </p>
          <Input
            class="flex w-full h-14 px-3 pt-5 rounded-lg bg-primary-foreground/50 transition-colors file:border-0 focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-border disabled:cursor-not-allowed focus-visible:bg-primary-foreground disabled:opacity-50 input  placeholder:opacity-50 "
            type="email"
            id="email"
            placeholder="Email"
          />
        </div>
        <div class="relative">
          <p
            class="absolute left-3 top-2 text-xs leading-4 font-medium opacity-50"
          >
            รหัสผ่าน | Password
          </p>
          <Input
            class="flex w-full h-14 px-3 pt-5 rounded-lg bg-primary-foreground/50 transition-colors file:border-0 focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-border disabled:cursor-not-allowed focus-visible:bg-primary-foreground disabled:opacity-50 input  placeholder:opacity-50 "
            id="password"
            bind:value={password}
            type={showPassword ? "text" : "password"}
            placeholder="Password"
          />
          <button
            type="button"
            class="absolute right-3 top-1/2 -translate-y-1/2"
            on:click={() => (showPassword = !showPassword)}
            aria-label={showPassword ? "ซ่อนรหัสผ่าน" : "แสดงรหัสผ่าน"}
          >
            <Icon
              icon={showPassword ? "mdi:eye-off" : "mdi:eye"}
              class="size-5 text-zinc-400"
            />
          </button>
        </div>
      </div>
    </div>

    <div class="flex justify-end">
      <a href="/" class="text-sm text-zinc-400 hover:underline">ลืมรหัสผ่าน?</a>
    </div>

    <Button
      on:click={handleLogin}
      class="w-full"
      disabled={isLoading}
    >
      {#if isLoading}
        <Icon icon="mdi:loading" class="mr-2 size-4 animate-spin" />
        กำลังเข้าสู่ระบบ...
      {:else}
        เข้าสู่ระบบ
      {/if}
    </Button>
  </div>

  <div class="flex justify-center">
    <a
      href="/"
      class="flex items-center gap-1 text-sm text-zinc-400 hover:text-white"
    >
      <Icon icon="mdi:arrow-left" class="size-4" />
      กลับไปยังหน้าหลัก
    </a>
  </div>
</div>
