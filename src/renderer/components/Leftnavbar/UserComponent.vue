<template>
    <div class="user">
        <div class="avatar">
            <img :src="user.avatar" draggable="false"/>
        </div>
    </div>
</template>

<script>
export default {
  name: 'left-navbar',
  data () {
    return {
      user: {
        name: '',
        avatar: 'https://avatars0.githubusercontent.com/u/20413875?s=460&v=4'
      }
    }
  }
}
</script>
<style scoped>
  .user {
      width: 100%;
      height: 120px;
      display: flex;
      align-items: center;
      justify-content: center;
  }
  .user .avatar {
      width: 70px;
      height: 70px;
      border-radius: 50%;
      overflow: hidden;
      border: 2px solid #B3C0D1;
      box-shadow: 0px 0px 30px 5px;
  }
  .user .avatar img {
      -webkit-app-region: no-drag;
      width: 100%;
      height: 100%;
  }
</style>


