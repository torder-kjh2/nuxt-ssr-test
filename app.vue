<template>
  <div>
    {{count}}
  </div>
  <div>
    {{double}}
  </div>
  <button @click="()=>{count+=1}">
    증가
  </button>
</template>

<script lang="ts" setup>

const count = ref(1);

const double = computed(()=>count.value*2);

</script>