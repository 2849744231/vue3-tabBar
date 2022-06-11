# vue3-tabBar
封装组件tabBar呼Ψ(￣∀￣)Ψ，具体简单的cv，怎么使用，会说的，咩！
# 引入组件
直接把目录里的，components\common\tabbar移动到自己的组件里就可以
# 如何使用
点击进入，入口文件MainTabBar.vue

<TabBarItem path="/home" activeColor="#fc5979">
 // path决定怎么跳转，activeColor激活时，字体颜色
            <template #item-icon>
              //这里是没有激活时，显示的图片
                <img src="@/assets/imgs/tabbar/home.png" />
            </template>
            <template #item-icon-active>
               //这里是激活时，显示的图片
                <img src="@/assets/imgs/tabbar/home_active.png"/>
            </template>
            <template #item-text>
              //这里是tabBar的文字内容
                <div>首页</div>
            </template>         
        </TabBarItem>
