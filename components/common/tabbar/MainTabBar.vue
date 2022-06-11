<template>   
    <div id="tabbar">
        <!--这里path跳转路径，activeColor激活时，显示的文字-->
        <TabBarItem path="/home" activeColor="#fc5979">
            <template #item-icon>
                <!-- 没有激活时，的图片 -->
                <img src="@/assets/imgs/tabbar/home.png" />
            </template>
            <template #item-icon-active>
                <!-- 激活时，的图片  -->
                <img src="@/assets/imgs/tabbar/home_active.png"/>
            </template>
            <template #item-text>
                <!-- tabBar的文字 -->
                <div>首页</div>
            </template>         
        </TabBarItem>
        <!-- 当然，后面也可以添加多个的 -->
        <TabBarItem path="/category" activeColor="#fc5979">
            <template #item-icon>
                <img src="@/assets/imgs/tabbar/category.png" />
            </template>
            <template #item-icon-active>
                <img src="@/assets/imgs/tabbar/category_active.png"/>
            </template>
            <template #item-text>
                <div>分类</div>
            </template>         
        </TabBarItem>
    </div>
  
      
</template>

<script>

import TabBarItem from "@/components/common/tabbar/TabBarItem";

export default {
    name: "MainTabBar",
    components: {
        TabBarItem,
    },
};
</script>
<style lang="less" scoped>
#tabbar{
    display:flex;
    position: fixed;
    bottom: 0;left: 0;
    width: 100%;
    justify-content: space-around;
    box-shadow: 0 31px 51px #000;


}
</style>
