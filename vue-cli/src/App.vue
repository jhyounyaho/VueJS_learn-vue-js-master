<template>
  <div>
    <!-- v-bind로 props data 넘겨줌 -->
    <app-header 
      v-bind:propsdata='str'
      v-on:renew='renewStr'
    ></app-header>
  </div>  
</template>

<script>
import AppHeader from './components/AppHeader.vue';
/*
  let AppHeader = {
    template: '<header><h1>AppHeader</h1></header>
  }
  와 같은 결과물 
*/

export default {
  data: function() {
    return {
      str: 'Header',
    }
  },
  components: {
    'app-header': AppHeader,
  },
  methods: {
    renewStr: function() {
      this.str = this.str.split('').reverse().join('');
    },
  },
}
</script>

<style>

</style>