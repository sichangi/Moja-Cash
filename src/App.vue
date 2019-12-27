<template>
  <main>
    <symbols/>
    <navigation/>
    <core/>
    <foot/>
  </main>
</template>

<script>
  import Navigation from './components/navigation';
  import Core from './components/core';
  import Foot from './components/foot';
  import Symbols from './components/symbols';

  export default {
    name: 'Moja',
    components: {Symbols, Navigation, Core, Foot}
  };
</script>

<style lang="scss" src="./assets/styles/main.scss"/>
