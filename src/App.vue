<script setup lang="ts">
import { ref,Ref,reactive } from 'vue';
interface C {
  d:string
}
let a:number = 6666
const b:Ref<string> = ref('b')
setTimeout(() => {
  b.value = 'bbbbb'
}, 1000);
const c:C = reactive({
  d: 'ccc'
})
setTimeout(() => {
  c.d = 'ddddddd'
}, 1000);
</script>

<template>
  <div>
    {{a}}
    <br>
    {{ b }}
    <br>
    {{ c.d }}
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
