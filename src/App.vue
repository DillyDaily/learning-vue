<template>
  <div id="app">
    <div class="container">
      <life-header></life-header>
    </div>
    <div class="container">
      <life-admin></life-admin>
    </div>
    <div class="container">
      <life-footer></life-footer>
    </div>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import Home from './components/Home.vue'
import Menu from './components/Menu.vue'
import Admin from './components/Admin.vue'

export default {
  components: {
    lifeHeader: Header,
    lifeFooter: Footer,
    lifeHome: Home,
    lifeMenu: Menu,
    lifeAdmin: Admin,
  }
}
</script>

<style>

</style>
