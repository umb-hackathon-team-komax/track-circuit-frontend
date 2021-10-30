<template>
<div>
  <Header/>
  <div class="grid grid-rows-3 grid-cols-5 m-8 gap-4">
    <Infos class="row-span-1 row-end-1"/>
    <Output class="row-span-5 col-span-4"/>
    <Counter class="row-span-3"/>
    <Infos2 class=""/>
  </div>
</div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Header from './components/Header.vue'
import Counter from './components/Counter.vue'
import Output from  './components/Output.vue'
import Infos from './components/Infos.vue'
import Infos2 from  './components/Infos2.vue'

export default defineComponent({
  name: 'App',
  components: {
    Header,
    Counter,
    Output,
    Infos,
    Infos2
  }
});
</script>

<style lang="scss">

</style>
