<template>
  <div class="header">
    <div class="content">
      <slot name="content">
        <HeaderNavBar :nav-list="navTitleList"></HeaderNavBar>
      </slot>
    </div>
  </div>
</template>

<script>
  export default {
    name : 'Header',
    
    data () {
      return {
        navTitleList : [
          {
            title : '首页',
            link : '/'
          },
          {
            title : '关于',
            link : '/about'
          },
          {
            title : '加入',
            link : '/join'
          },
        ]
      }
    }
  }
</script>

<style scoped>
  .header {
    width: 100%;
    height: 52px;
    position: relative;
    z-index: 100;
    box-shadow: 0 1px 3px rgba(18,18,18,.1);
  }

  .content {
    width: 80%;
    margin: 0 auto;
    overflow: hidden;
  }
</style>