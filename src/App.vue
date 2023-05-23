<script setup lang="ts">
// imports
import { onMounted } from 'vue';
import emojis from 'emojibase-data/en/data.json'

// methods
function showEmoji(emoji: string) {
  alert(emoji)
}

// mounted
onMounted(() => {
  console.log(emojis)
})

</script>

<template>
  <div class="app">
    <pre v-for="e of emojis">
      <span class="emoji" @click="showEmoji(e.emoji)">{{ e.emoji }}</span>
    </pre>
  </div>
</template>

<style scoped lang="scss">
.app {
  padding: 5px;
    & .emoji {
      user-select: none;
      cursor: pointer;
    }
}
</style>
