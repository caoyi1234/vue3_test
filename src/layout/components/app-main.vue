<template>
  <section class="app-main">
    <transition name="fade-transform" mode="out-in">
      <keep-alive :include="cachedViews">
        <Header/>
        <router-view :key="key" />
      </keep-alive>
    </transition>
  </section>
</template>

<script>
import Header from './header/index'
export default {
  name: 'app-main',
  components:{
    Header
  },
  setup() {
  },
};
</script>