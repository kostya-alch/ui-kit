<template>
  <div class="container">
    <Header />
    <sidebar />
    <div class="content">
      <router-view />
    </div>
  </div>
</template>

<script setup lang="ts">
import Header from '@/layout/Header.vue';
import Sidebar from '@/components/Sidebar.vue';
</script>

<style lang="scss">
@import './styles/globals.scss';

#app {
  font-family: Avenir, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.content {
  max-width: 1400px;
  margin-left: 250px;
  padding: 30px;
  transition: 0.2s;

  &_full {
    margin-left: 0;
  }
}
</style>
