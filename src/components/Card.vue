<script setup>

  const props = defineProps({
    topImg: { type: String, required: false },
    botImg: { type: String, required: false }, 
    mainImg: {type: String, required: false},
    type: {type: String, required: true},
    name: {type: String, required: true},
    vendorСode: { type: String, required: true },
    price: { type: String, required: true }
  });
</script>

<template>
   <div class="w-fit">
    <div class="relative">
        <img v-if="topImg" class="absolute top-3 left-3" :src="`/${topImg}.svg`" alt="topImg">
        <img :src="mainImg" :alt="mainImg">
        <img v-if="botImg" class="absolute bottom-3 right-3" :src="`/${botImg}.svg`" alt="topImg">
    </div>
      <div class="px-[13px] py-[15px] bg-[#EFF5F5]">
        <p class="text-[#6E6659] text-sm font-light">{{ type }}</p>
        <h3 class="color-[#264E58] text-lg font-semibold">{{ name }}</h3>
        <p class="text-[#A5A5A5]">Артикул: <span class="text-[#264E54]">{{ vendorСode }}</span></p>
        <p class="text-[#A5A5A5] text-2xl">от: <span class="text-[#6E6659] font-bold">{{ price }}</span> Р</p>
    </div>
   </div>
</template>