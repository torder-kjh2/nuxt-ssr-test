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
  <Sample v-if="flag"/>
  <button @click="()=>{flag = !flag}">쇼미 컴포넌트</button>
  
</template>

<script lang="ts" setup>

import Sample from './components/Sample.vue'

const title = ref('My App')
const description = ref('My App Description')

useHead({
  title,
  meta: [{
    name: 'description',
    content: description
  }]
})

const count = ref(1);

const double = computed(()=>count.value*2);

const flag = ref(false);

</script>