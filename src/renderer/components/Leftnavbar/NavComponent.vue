<template>
    <ul>
        <li v-for="(item, index) in menus" :key="index">
            <router-link 
              :to="item.link" 
              class="nav-link">{{ item.text }}</router-link>
        </li>
    </ul>
</template>

<script>
export default {
  props: ['MenusData'],
  name: 'left-navbar',
  data () {
    return {
      menus: []
    }
  },
  mounted () {
    this.menus = this.MenusData
  }
}
</script>
<style scoped>
  li {
    line-height: 35px;
    text-align: left;
    box-sizing: border-box;
    padding-left: 20px;
    font-size: 14px;
  }
  li .nav-link {
    display: block;
  }
</style>

