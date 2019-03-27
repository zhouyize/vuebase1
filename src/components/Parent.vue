<template>
    <!--只能存在一个根容器-->
    <div class="parent">
      父组件：{{money}}
      <Child @money="getMoney" parent="王健林" nick="娱乐圈纪检委" :age="age" title="一个小目标：一个亿"/>
    </div>
</template>

<script>

    import Child from './Child'

    export default {
        name: 'parent',
        props: [],
        //所有的初始化状态全部放入data中
        data() {
            return {
              money:'',
              age:30
            }
        },
        methods: {
          getMoney(data){
            this.money=data
          }
        },
        //计算属性
        computed: {},

        //实时监听数据变化，可以在这里做相关判断
        watch: {},

        components: {
          Child
        }
    }
</script>

<!--样式-->
<!--
Add "scoped" attribute to limit CSS to this component only
添加scoped属性限制样式只在当前组件中生效
-->
<style>

</style>
