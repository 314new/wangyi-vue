<template>
    <div class="welcome">
        <el-container>
            <el-aside class="coustom-scroll-bar" style="width: 200px">
                <leftnavbar />
            </el-aside>
            <el-container>
                <el-header>
                    <headerbar />
                </el-header>
                <el-main>
                    
                </el-main>
                <el-footer>
                    
                </el-footer>
            </el-container>
        </el-container>
    </div>
</template>

<script>
import Leftnavbar from './Leftnavbar/Leftnavbar'
import Headerbar from './Headerbar/Headerbar'
export default {
  name: 'welcome',
  components: {
    Leftnavbar,
    Headerbar
  },
  data () {
    return {}
  }
}
</script>

<style scoped>
  .welcome {
    width: 100%;
    height: 100%;
  }
  .el-container {
    width: 100%;
    height: 100%;
  }
  .el-header, .el-footer {
    -webkit-app-region: drag;
    text-align: center;
    line-height: 60px;
    background-color: #B3C0D1;
    color: #333;
  }
  
  .el-aside {
    background-color: #D3DCE6;
    color: #333;
    text-align: center;
  }
  
  .el-main {
    background-color: #E9EEF3;
    color: #333;
    text-align: center;
  }

  .el-container:nth-child(5) .el-aside,
  .el-container:nth-child(6) .el-aside {
    line-height: 260px;
  }
  
  .el-container:nth-child(7) .el-aside {
    line-height: 320px;
  }
</style>


