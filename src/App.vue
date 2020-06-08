<template>
  <div id="app">
    <button v-on:click="active=!active">切り替え</button>
    <transition name="fade">
      <p v-if="active">わっしょい</p>
    </transition>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      active:false
    }
  },
  methods:{
    onClick(){
      this.active=!this.active
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.fade-enter-active, .fade-leave-active {
  transition: opacity 1s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
