<script setup>
  import { ref } from 'vue';

  const props = defineProps({
    title: { type: String, required: true },
    ariaTitle: { type: String, required: true },
    description: { type: String, required: true }
  });

  const showPanel = ref(false);

  const togglePanel = () => {
    showPanel.value = !showPanel.value;
  };
</script>

<template>
  <div class="text-[#283F75] mb-[20px] w-[460px] hover:scale-105 transition-all duration-300">
    <button
      :arial-controls="'accordion-content-' + ariaTitle"
      :id="'accordion-control-' + ariaTitle"
      @click.prevent="togglePanel"
      class="border-[#C6CDDA] border py-[20px] px-[30px] w-full flex justify-between items-center">
      {{ title }}
      <span class="material-icons">
        <img :class="{ 'rotate-180': showPanel }" src="/Down.svg" alt="">
      </span>
    </button>
    <div
      :aria-hidden="!showPanel"
      :id="'content-' + ariaTitle"
      class="p-4 max-w-fit w-full"
      v-if="showPanel">
      {{ description }}
    </div>
  </div>
</template>
