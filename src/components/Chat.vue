<script setup lang="ts">
export type ChatItem = {
  name: string;
  position?: "start" | "end";
  image: string;
  message: string;
  time: string;
};

interface Props {
  items: ChatItem[];
}

defineProps<Props>();
</script>

<template>
  <div>
    <div
      v-for="(item, index) in items"
      :key="index"
      class="chat"
      :class="[
        { 'chat-start': item.position === 'start' },
        { 'chat-end': item.position === 'end' },
      ]"
    >
      <div class="chat-image avatar">
        <div class="w-10 rounded-full">
          <img :alt="item.name" :src="item.image" />
        </div>
      </div>

      <div class="chat-header">
        {{ item.name }}
        <time class="text-xs opacity-50">{{ item.time }}</time>
      </div>

      <div class="chat-bubble">
        {{ item.message }}
      </div>

      <div class="chat-footer opacity-50">Okady</div>
    </div>
  </div>
</template>
