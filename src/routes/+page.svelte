<script lang="ts">
  import { Button } from "$lib/components/ui/button/index.js";
  import Icon from "@iconify/svelte";
  import logo from "$lib/images/logo.png";
  import * as Carousel from "$lib/components/ui/carousel/index.js";

  let username = "Bossnz";
</script>

<div class="flex flex-col w-full items-center justify-center gap-4 mt-24">
  <img src={logo} alt="WarpLKB" class="w-fit h-20" />
  <p class="text-white font-semi text-xl">ยินดีต้อนรับเข้าสู่ร้าน WarpLKB</p>
  <!-- อันนี้จะแสดงเมื่อ login เสร็จ get username มาแสดง -->
   
  <div class="flex items-center gap-2">
    <p>🙏 สวัสดีคุณ</p>
    <p
      class="font-medium text-transparent bg-gradient-to-r from-pink-500 to-rose-500 bg-clip-text"
    >
      {username}
    </p>
  </div>

  <!-- ------------------------------- -->

  <div class="flex justify-between items-center w-full gap-4">
    <div class="flex items-center gap-2">
      <Icon
        icon="fluent:ticket-diagonal-20-regular"
        class="size-8 text-rose-500"
      />
      <div>
        <p class="">คอนเสิร์ตที่จะมาถึง</p>
        <p class="text-sm text-zinc-400">Concert</p>
      </div>
    </div>
    <Button variant="outline" size="icon" class="">
      <Icon icon="iconamoon:arrow-right-2-light" class="size-8" />
    </Button>
  </div>
  <div class="bg-border/50 w-full h-0.5 rounded-xl"></div>
  <Carousel.Root class="w-full overflow-hidden">
    <Carousel.Content class="flex w-1/2">
      <Carousel.Item>
        <img
          src="https://s3-ap-southeast-1.amazonaws.com/tm-img-poster-event/c78d92c0dc7211ed911101117567899b.jpg"
          alt="concert1"
          class="w-full h-60 object-cover rounded-xl"
        />
      </Carousel.Item>
      <Carousel.Item>
        <img
          src="https://scontent.fbkk5-5.fna.fbcdn.net/v/t39.30808-6/466900412_979394320878631_1762369586111409187_n.jpg?_nc_cat=100&ccb=1-7&_nc_sid=127cfc&_nc_ohc=ljww1Y5ifKoQ7kNvgGC8h0r&_nc_oc=AdgNOB0tXIEQDpKMzFgtGxhEV3UBtHSGF-HgW6x1cNxE51kb2NZTn8CRaFNfN37Tbz0&_nc_zt=23&_nc_ht=scontent.fbkk5-5.fna&_nc_gid=ARlEKqNCNMa8ayN_iQfnLVd&oh=00_AYGgq-v3Jljob7FjWp-1E6PGKjpRzVwIoxcgob-qxRQ32g&oe=67DA2E53"
          alt="concert2"
          class="w-full h-60 object-cover rounded-xl"
        />
      </Carousel.Item>
      <Carousel.Item>
        <img
          src="https://res.theconcert.com/w_534,h_712,c_thumb/933e39dbb1c3f420565ccf55bd9dea6d8/449673905_484865680952547_4062294729871614624_n.jpg"
          alt="1"
          class="w-full h-60 object-cover rounded-xl"
        />
      </Carousel.Item>
    </Carousel.Content>
  </Carousel.Root>
  <div class="flex w-full items-center gap-2">
    <Icon icon="mynaui:grid" class="size-8 text-rose-500" />
    <div>
      <p class="">เมนูต่างๆ</p>
      <p class="text-sm text-zinc-400">Menu</p>
    </div>
  </div>
  <div class="bg-border/50 w-full h-0.5 rounded-xl"></div>
  <div class="flex flex-col gap-2 w-full">
    <button
      class="flex flex-wrap text-start items-center bg-primary-foreground/75 text-white text-xl p-4 space-x-2 rounded-lg hover:bg-primary-foreground hover:ring-[1px] hover:ring-gray-800"
    >
      <Icon icon="emojione:clinking-beer-mugs" class="size-8 " />
      <div>
        <p>รายการเครื่องดื่ม</p>
        <p class="text-xs text-gray-400">สั่งเครื่องและอาหารในร้านได้เลย</p>
      </div>
    </button>
    <div class="flex gap-2">
      <button
        class="flex w-full text-start items-center bg-primary-foreground/75 text-white text-xl p-4 space-x-2 rounded-lg hover:bg-primary-foreground hover:ring-[1px] hover:ring-gray-800"
      >
        <Icon icon="emojione:pushpin" class="size-8" />
        <div>
          <p class="text-start">จองโต๊ะ</p>
          <p class="text-xs text-gray-400">จองโต๊ะล่วงหน้าได้เลย</p>
        </div>
      </button>
      <button
        class="flex w-full text-start items-center bg-primary-foreground/75 text-white text-xl p-4 space-x-2 rounded-lg hover:bg-primary-foreground hover:ring-[1px] hover:ring-gray-800"
      >
        <Icon icon="emojione:admission-tickets" class="size-8" />
        <div>
          <p class="text-start">ซื้อตั๋วคอนเสิร์ต</p>
          <p class="text-xs text-gray-400">ดูคอนเสิรต์ที่น่าสนได้เลย</p>
        </div>
      </button>
    </div>
    <button
      class="flex flex-wrap text-start items-center bg-primary-foreground/75 text-white text-xl p-4 space-x-2 rounded-lg hover:bg-primary-foreground hover:ring-[1px] hover:ring-gray-800"
    >
      <Icon icon="emojione:framed-picture" class="size-8 " />
      <div>
        <p>ส่งรูปขึ้นจอ</p>
        <p class="text-xs text-gray-400">เปิดวาร์ปไอจีและรูปในร้านได้เลย</p>
      </div>
    </button>
  </div>
</div>
