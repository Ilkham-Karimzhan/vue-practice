<template>
  <div class="app-main-layout">

    <Navbar @click="isOpen = !isOpen" />

    <Sidebar v-model="isOpen" />

    <main class="app-content" :class="{full: !isOpen}">
      <div class="app-page">
        <router-view/>
      </div>
    </main>

    <div class="fixed-action-btn">
      <a class="btn-floating btn-large blue" href="#">
       <i class="large material-icons">add</i>
      </a>
    </div>
  </div>
</template>

<script> // eslint-disable-next-line
import Navbar from '@/components/app/Navbar-com.vue'; // eslint-disable-next-line
import Sidebar from '@/components/app/Sidebar-com.vue'; // eslint-disable-next-line

export default {
  name: 'main-layout',
  data: () => ({
    isOpen: true
  }),
  components: {
    Navbar, Sidebar
  }
}
</script>
