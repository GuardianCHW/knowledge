<template>
    <div>
        <header>
            <div class="header_middel">
                <div class="header_logo"></div>
                <div class="header_option">
                    <ul>
                        <li v-for="(item,indexSelect) in navOptions" @click="select(indexSelect)" :class="indexSelect == navOptionsIndex?'active':''" :key="indexSelect" v-text="item"></li>
                    </ul>
                </div>
            </div>
        </header>
        <main>
            <div>
                <div class="Rotation">

                </div>
                <div>
                    
                </div>
            </div>
        </main>
    </div>
</template>

<script>

export default {
  name: "Index",
  components: {
    //   注册组件
  },
  data(){
      return{
          navOptions:["首页","博客","留言","日记","关于"],
          navOptionsIndex:0,
      }
  },
  created(){
    //   在模板渲染成html前调用，即通常初始化某些属性值，然后再渲染成视图，实例创建完后立刻被调用，$el属性目前不可见
  },
  mounted(){
    //   在模板渲染成html后调用，通常是初始化页面完成后，再对html的dom节点进行一些需要的操作
  },
  computed:{
    //   计算属性
  },
  methods:{
      select(index){
          var _this = this
          _this.navOptionsIndex = index
      },
  },
};
</script>

<style lang="less" scoped>
    @theme_color:#aqua;
    header{
        width: 100%;
        height: 6rem;
        background-color: #f6f;
        color: #fff;
        .header_middel{
            width: 70%;
            height: 100%;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            .header_logo{
                background-color: beige;
                width: 10rem;
                height: 100%;
            }
            .header_option{
                width: 60%;
                ul{
                    display: flex;
                    li{
                        width: 7.5rem;
                        height: 100%;
                        line-height: 6rem;
                        background-color: #c3c;
                    }
                    li:hover{
                        background-color: blueviolet;
                    }
                    .active{
                        background-color: blueviolet;
                    }
                }
            }
        }
    }
</style>
