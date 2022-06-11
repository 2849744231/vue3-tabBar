<template>
  <router-view />
  <MainTabBar></MainTabBar>
</template>

<script>

import MainTabBar from "@/components/common/tabbar/MainTabBar";


export default {
  name: 'App',
  data(){
    return {
     
    }
  },
  components: {
    MainTabBar
  }
}
</script>

<style>

</style>
