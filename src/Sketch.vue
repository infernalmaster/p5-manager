<template lang="pug">
  iframe(v-bind:src='src' width='100%' scrolling='no')
</template>

<script>
  import Vue from 'vue'
  import VueRouter from 'vue-router'
  Vue.use(VueRouter);

  export default {
    data() {
      return {
      }
    },
    props: ['project', 'propsA'],
    computed: {
      src() {
        return '/' + this.project + '/index.html'
      }
    }

  }
</script>

<style lang="scss">
  iframe {
    border: none;
    height: 100%;
    margin-left: 0px;
  }
</style>
