<template>
    <div class="header">
        <i v-for="(item, index) in icons" 
            :key="index"
            :class="['do-window', commonClass, item.selfClass, item.iconClass]"></i>
    </div>
</template>

<script>
import electron from 'electron'
import icons from './../../assets/data/window.json'
export default {
  name: 'left-navbar',
  data () {
    return {
      commonClass: icons.commonClass,
      icons: icons.HeaderBarIcon
    }
  },
  mounted () {
    const win = electron.remote.getCurrentWindow()
    const map = {
      isMax: false
    }

    let small = document.querySelector('.small')
    small.addEventListener('click', function () {
      win.minimize()
    })

    let full = document.querySelector('.full')
    full.addEventListener('click', function () {
      if (map.isMax) {
        document.documentElement.style.padding = 5 + 'px'
        win.unmaximize()
        map.isMax = false
      } else {
        document.documentElement.style.padding = 0 + 'px'
        win.maximize()
        map.isMax = true
      }
    })

    let close = document.querySelector('.close')
    close.addEventListener('click', function () {
      if (process.platform !== 'darwin') {
        electron.remote.app.quit()
      }
    })
  }
}
</script>
<style scoped>
  .header {
    display: flex;
    justify-content: flex-end;
  }
  .header i {
    -webkit-app-region: no-drag;
    font-size: 18px;
    margin: 0 3px;
  }
  .header i:hover {
    text-shadow: 0 0 7px #000;
  }
  .small {
    color: #FFD740
  } 
  .full {
    color: #FF9100
  }
  .close {
    color: #E65100
  } 

</style>


