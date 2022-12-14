<template>
  <div class="sidebar">
    <router-link class="sidebar__link" v-for="link in links" :key="link.name" :to="link.href"
      >{{ link.name }}
    </router-link>
  </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue';

const links = ref([
  { name: 'Typography', href: '/typography' },
  {
    name: 'Button',
    href: '/button',
  },
]);
</script>

<style scoped lang="scss">
.sidebar {
  left: 0;
  height: 100%;
  top: 62px;
  background: #fff;
  position: fixed;
  width: 250px;
  padding: 20px;
  transition: 0.2s;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.07);
  transform: translateX(0px);

  &__link {
    display: block;
    border-radius: 12px;
    padding: 10px;
    border: 2px solid #fff;
    transition: 0.2s;
    font-weight: bold;
    margin-bottom: 10px;

    &:hover {
      border-color: var(--primary-color);
    }
  }
}
</style>
