<template>
<div>
  <Header/>
  <div class="grid grid-rows-3 grid-cols-5 m-8 gap-4">
    <Counter class="row-span-1 row-end-1"/>
    <Output class="row-span-3 col-span-3"/>
  </div>
</div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Header from './components/Header.vue'
import Counter from './components/Counter.vue'
import Output from  './components/Output.vue'

export default defineComponent({
  name: 'App',
  components: {
    Header,
    Counter,
    Output
  }
});
</script>

<style lang="scss">

</style>
