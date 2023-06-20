<template>
  <div>{{ msg }}</div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  setup() {
    const msg = ref('');
    const b64 = Buffer.from('Hello David Myers').toString('base64');
    msg.value = Buffer.from(b64, 'base64').toString('ascii');
    return {
      msg,
    };
  },
});
</script>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
