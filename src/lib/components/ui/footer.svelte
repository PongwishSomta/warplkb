<script>
  export let year = new Date().getFullYear();
</script>

<footer
  class="w-full bg-background text-white py-6 px-4 mt-10 border-t border-border"
>
  <div class="max-w-5xl mx-auto flex flex-col items-center space-y-4">
    <!-- โลโก้ หรือ ชื่อเว็บ -->
    <div>WarpLKB</div>

    <!-- เมนูใน Footer -->
    <nav class="flex space-x-6 text-sm">
      <a href="/" class="hover:text-rose-500 transition-colors">หน้าแรก</a>
      <a href="/" class="hover:text-rose-500 transition-colors">บริการ</a>
      <a href="/backoffice-login" class="hover:text-rose-500 transition-colors">จัดการร้าน</a>
    </nav>

    <!-- ลิขสิทธิ์ -->
    <div class="text-sm text-gray-400">
      &copy; {year} WarpLKB. All rights reserved.
    </div>
  </div>
</footer>
