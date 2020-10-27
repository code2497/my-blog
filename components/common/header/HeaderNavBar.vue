<template>
  <ul class="nav">
    <li v-for="(item,index) in navList" 
    :key="item.title"
    @click="curIndex=index"
    :class="{active : curIndex==index}">
      <NuxtLink :to="item.link">{{item.title}}</NuxtLink>
    </li>
  </ul>
</template>

<script>
  export default {
    name : 'HeaderNavBar',
    props: {
      navList : {
        type : Array,
        default () {
          return [];
        }
      }
    },
    data () {
      return {
        curIndex : 0
      }
    }
  }
</script>

<style scoped>
  .nav li{
    float: left;
    line-height: 52px;
    margin-right: 20px;
    text-align: center;
  }

  .nav {
    float: left;
  }

  .nav li a {
    padding: 0 2px;
    padding-bottom: 5px;
    color: #8590a6;
  }

  .nav li .active:hover {
    color: #000!important;
  }

  .nav li a:hover {
    color: #777!important;
  }

  .active {
    border-bottom: 2px solid #0084ff;
    color: #000!important;
    font-weight: 500;
  }
</style>