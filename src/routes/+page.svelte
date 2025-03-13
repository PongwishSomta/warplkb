<script lang="ts">
  import { Button } from "$lib/components/ui/button/index.js";
  import Icon from "@iconify/svelte";
</script>

<div class="flex items-center justify-center">
  <div class="flex flex-col max-w-5xl text-center gap-4">
    <h1
      class="text-transparent font-bold text-5xl bg-clip-text bg-gradient-to-r from-pink-500 to-rose-500"
    >
      Welcome to WarpLKB
    </h1>
    <p class="text-white font-semi text-xl">ยินดีต้อนรับเข้าสู่ร้าน WarpLKB</p>
    <div class="bg-zinc-800 w-full h-0.5 rounded-xl"></div>
    <div class="flex justify-center gap-4">
      <Button
        class="w-full h-fit bg-primary-foreground/75 text-white text-base py-3 hover:bg-primary-foreground hover:ring-[1px] hover:ring-gray-800 "
        href="/login"
      >
        <p>เข้าสู่ระบบ</p>
      </Button>
      <Button
        class="w-full h-fit bg-primary-foreground/75 text-white text-base py-3 hover:bg-primary-foreground hover:ring-[1px] hover:ring-gray-800 "
        href="/register"
      >
        <p>สมัครสมาชิก</p>
      </Button>
    </div>
    <div
      class="flex gap-2 bg-gradient-to-r from-pink-500 via-rose-500/30 to-rose-500/0"
    >
      <div class="bg-white w-1 h-10 rounded-md"></div>
      <p class="my-auto">เลือกสิ่งที่คุณต้องการ</p>
    </div>
    <button
      class="flex flex-wrap bg-primary-foreground/75 text-white text-xl p-4 space-x-2 rounded-lg hover:bg-primary-foreground hover:ring-[1px] hover:ring-gray-800"
    >
      <Icon icon="healthicons:alcohol-outline" class="size-10" />
      <div>
        <p>รายการเครื่องดื่ม</p>
        <p class="text-xs text-gray-400">ดูรายการอาหารและเครื่องดื่ม</p>
      </div>
    </button>
    <button
      class="flex flex-wrap bg-primary-foreground/75 text-white text-xl p-4 space-x-2 rounded-lg hover:bg-primary-foreground hover:ring-[1px] hover:ring-gray-800"
    >
      <Icon icon="healthicons:alcohol-outline" class="size-10" />
      <div>
        <p>รายการเครื่องดื่ม</p>
        <p class="text-xs text-gray-400">ดูรายการอาหารและเครื่องดื่ม</p>
      </div>
    </button>
  </div>
</div>
