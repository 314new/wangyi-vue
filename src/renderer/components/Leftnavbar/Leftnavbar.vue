<template>
    <div class="left-navbar">
      <user-component />
      <div class="nav fg-nav">
        <nav-component :menus-data="firstNavGroup"/>
      </div>
      <div class="nav fg-nav">
        <nav-component :menus-data="secondtNavGroup"/>
      </div>
    </div>
</template>

<script>
import NavComponent from './NavComponent'
import UserComponent from './UserComponent'
import navbar from './../../assets/data/navbar.json'
export default {
  name: 'left-navbar',
  components: {
    NavComponent,
    UserComponent
  },
  data () {
    return {
      firstNavGroup: navbar.FG,
      secondtNavGroup: navbar.SG
    }
  }
}
</script>
<style scoped>
  .left-navbar {
    user-select: none;
  }
  .nav {
    margin-bottom: 40px;
  }
</style>


