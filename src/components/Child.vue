
<template>
    <!--只能存在一个根容器-->
    <div class="child">
      {{getFoo}}
      子组件：{{title}}-{{age}}
      <p>称号：{{nick }}</p>
      <p>父亲：{{parent}}</p>
      <p>女朋友们:</p>
      <ul>
        <li v-for="girl in girlFriends">{{girl}}</li>
      </ul>
      <button @click="sendMoney" type="button" name="button">赚了</button>
    </div>
</template>

<script>
    export default {
        name: 'child',
        //props: ["title","age"],
        props:{
          title:String,
          age:Number,
          nick:{
            type:String,
            default:'国民老公'
          },
          parent:{
            type:String,
            required:true
          },

          // 对象或数组默认值必须从一个工厂函数获取
          girlFriends:{
            type:Array,
            default:function(){
              return ['g1','g2']
            }
          }
        },

        //所有的初始化状态全部放入data中
        data() {
            return {}
        },
        methods: {
          sendMoney(){
            this.$emit("money","翻了5倍")
          }

        },
        //计算属性
        computed: {
          getFoo(){
            return this.$root.foo
          }
        },

        //实时监听数据变化，可以在这里做相关判断
        watch: {}

    }
</script>

<!--样式-->
<!--
Add "scoped" attribute to limit CSS to this component only
添加scoped属性限制样式只在当前组件中生效
-->
<style>

</style>
