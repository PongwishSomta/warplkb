<script lang="ts">
  import { Input } from "$lib/components/ui/input/index.js";
  import { Button } from "$lib/components/ui/button/index.js";
  import { Checkbox } from "$lib/components/ui/checkbox/index.js";
  import { Label } from "$lib/components/ui/label/index.js";
</script>

<div class="space-y-4 w-full">
  <div class="relative">
    <p class="absolute left-3 top-2 text-xs leading-4 font-medium opacity-50">
      ชื่อผู้ใช้งาน | Username
    </p>
    <Input
      class="flex w-full h-14 px-3 pt-5 rounded-lg bg-primary-foreground/50 transition-colors file:border-0 focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-border disabled:cursor-not-allowed focus-visible:bg-primary-foreground disabled:opacity-50 input  placeholder:opacity-50 "
      type="username"
      id="username"
      placeholder="Username"
    />
  </div>
  <div class="relative">
    <p class="absolute left-3 top-2 text-xs leading-4 font-medium opacity-50">
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
    <p class="absolute left-3 top-2 text-xs leading-4 font-medium opacity-50">
      รหัสผ่าน | Password
    </p>
    <Input
      class="flex w-full h-14 px-3 pt-5 rounded-lg bg-primary-foreground/50 transition-colors file:border-0 focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-border disabled:cursor-not-allowed focus-visible:bg-primary-foreground disabled:opacity-50 input  placeholder:opacity-50 "
      type="password"
      id="password"
      placeholder="Password"
    />
  </div>
  <div class="relative">
    <p class="absolute left-3 top-2 text-xs leading-4 font-medium opacity-50">
      รหัสผ่านอีกครั้ง | Re-Password
    </p>
    <Input
      class="flex w-full h-14 px-3 pt-5 rounded-lg bg-primary-foreground/50 transition-colors file:border-0 focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-border disabled:cursor-not-allowed focus-visible:bg-primary-foreground disabled:opacity-50 input  placeholder:opacity-50 "
      type="password"
      id="password"
      placeholder="Re-Password"
    />
  </div>
  <div class="flex items-center gap-2"> 
    <Checkbox id="terms" class="rounded-[4px]" />
    <Label
      for="terms"
      class="text-sm  leading-none peer-disabled:cursor-not-allowed peer-disabled:opacity-70"
    >
      อายุ 20 ปีขึ้นไป และยอมรับ ข้อตกลงและเงื่อนไข
    </Label>
  </div>

  <Button
    class="w-full h-fit bg-gradient-to-r from-pink-500 to-rose-500 text-white text-base py-3 hover:bg-gradient-to-r hover:from-pink-600 hover:to-rose-600 transition-colors "
    href="/#"
  >
    <p>สมัครสมาชิก</p>
  </Button>
  <p class="text-zinc-300 text-xs text-center">
    มีบัญชีอยู่แล้ว <a href="/login" class="underline">เข้าสู่ระบบ</a>
  </p>
  <div class="flex gap-2 items-center">
    <div class="bg-border w-full h-0.5 rounded-full"></div>
    <p class="text-zinc-500">หรือ</p>
    <div class="bg-border w-full h-0.5 rounded-full"></div>
  </div>
  <Button
    class="w-full h-fit bg-primary text-white text-base py-3 focus-visible:bg-secondary "
    href="/register"
  >
    <img
      src="https://cdn4.iconfinder.com/data/icons/logos-brands-7/512/google_logo-google_icongoogle-512.png"
      alt="Google"
      class="w-6 h-6"
    />
    <p class="text-zinc-800 ml-2">สมัครสมาชิกด้วย google</p>
  </Button>
</div>
